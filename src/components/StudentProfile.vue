<script setup>
    import { reactive } from 'vue'

    const student = reactive({
    course: 'Vue.js',
    name: 'John',
    age: 22,
    email: 'john@example.com'
    })

    const updateStudent = () => {
    student.name = 'Charles'
    student.course = 'Laravel'
    student.age = 25
    }

    const changeCourse = () => {
    student.course = 'Vue.js Advanced'
    }
</script>

<template>
  <div>
    <h2>Student Profile</h2>
    <p><strong>Name:</strong> {{ student.name }}</p>
    <p><strong>Course:</strong> {{ student.course }}</p>
    <p><strong>Age:</strong> {{ student.age }}</p>
    <p><strong>Email:</strong> {{ student.email }}</p>

    <button @click="updateStudent">Update Student</button>
    <button @click="changeCourse">Change Course</button>
  </div>
</template>