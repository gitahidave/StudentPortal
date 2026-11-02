<script setup>
    import { ref, reactive } from 'vue'

    const studentName = ref('')
    const studentAge = ref(0)

    const student = reactive({
    course: '',
    email: ''
    })

    const registerStudent = () => {
    studentName.value = 'Mary'
    studentAge.value = 21
    student.course = 'Vue.js'
    student.email = 'mary@example.com'
    }

    const changeCourse = () => {
    student.course = 'Laravel'
    }

    const resetForm = () => {
    studentName.value = ''
    studentAge.value = 0
    student.course = ''
    student.email = ''
    }
</script>

<template>
  <div>
    <h2>Student Registration Form</h2>
    <p><strong>Student Name:</strong> {{ studentName }}</p>
    <p><strong>Student Age:</strong> {{ studentAge }}</p>
    <p><strong>Course:</strong> {{ student.course }}</p>
    <p><strong>Email:</strong> {{ student.email }}</p>

    <button @click="registerStudent">Register Student</button>
    <button @click="changeCourse">Change Course</button>
    <button @click="resetForm">Reset</button>
  </div>
</template>