<template>
  <a-modal
    v-model:open="localVisible"
    title="Оставьте заявку"
    @ok="handleSubmit"
    @cancel="handleCancel"
  >
    <a-form
      ref="formRef"
      :model="formState"
      :rules="rules"
      layout="vertical"
    >
      <a-form-item label="Ваше имя" name="name">
        <a-input 
          v-model:value="formState.name"
          placeholder="Иван Иванов"
          size="large"
        />
      </a-form-item>

      <a-form-item label="Telegram / WhatsApp" name="contact">
        <a-input 
          v-model:value="formState.contact"
          placeholder="@username или +7..."
          size="large"
        />
      </a-form-item>
    </a-form>
  </a-modal>
</template>

<script setup>
import { ref, watch } from 'vue'
import { message } from 'ant-design-vue'

const props = defineProps({
  visible: Boolean
})

const emit = defineEmits(['update:visible', 'submit'])

const localVisible = ref(props.visible)
const formRef = ref()
const formState = ref({ name: '', contact: '' })

const rules = {
  name: [{ required: true, message: 'Введите имя', trigger: 'blur' }],
  contact: [{ required: true, message: 'Введите контакт', trigger: 'blur' }]
}

watch(() => props.visible, (val) => {
  localVisible.value = val
})

watch(localVisible, (val) => {
  emit('update:visible', val)
})

const handleSubmit = async () => {
  try {
    await formRef.value.validate()
    emit('submit', formState.value)
    formState.value = { name: '', contact: '' }
    localVisible.value = false
  } catch (error) {
    console.error('Validation failed:', error)
  }
}

const handleCancel = () => {
  formState.value = { name: '', contact: '' }
  localVisible.value = false
}
</script>