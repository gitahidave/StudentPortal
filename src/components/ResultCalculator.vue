<script setup>
    import { reactive, computed } from 'vue'

    const student = reactive({
    name: 'John',
    course: 'Vue.js',
    marks: 75
    })

    const result = computed(() => {
    if (student.marks >= 70 && student.marks <= 100) return 'Distinction'
    if (student.marks >= 60 && student.marks <= 69) return 'Credit'
    if (student.marks >= 50 && student.marks <= 59) return 'Pass'
    return 'Fail'
    })

    const increaseMarks = () => {
    student.marks += 5
    }

    const decreaseMarks = () => {
    student.marks -= 5
    }

    const resetMarks = () => {
    student.marks = 75
}
</script>

<template>
  <div>
    <h2>Student Result Calculator</h2>
    <p><strong>Name:</strong> {{ student.name }}</p>
    <p><strong>Course:</strong> {{ student.course }}</p>
    <p><strong>Marks:</strong> {{ student.marks }}</p>
    <p><strong>Result:</strong> {{ result }}</p>

    <button @click="increaseMarks">Increase Marks</button>
    <button @click="decreaseMarks">Decrease Marks</button>
    <button @click="resetMarks">Reset</button>
  </div>
</template>