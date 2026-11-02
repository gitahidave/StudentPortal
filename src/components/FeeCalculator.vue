<script setup>
    import { reactive, computed } from 'vue'

    const student = reactive({
    name: 'Mary',
    course: 'Vue.js',
    tuitionFee: 50000,
    amountPaid: 30000
    })

    const balance = computed(() => {
    return student.tuitionFee - student.amountPaid
    })

    const payFiveThousand = () => {
    student.amountPaid += 5000
    }

    const payTenThousand = () => {
    student.amountPaid += 10000
    }

    const resetPayment = () => {
    student.amountPaid = 30000
    }
</script>

<template>
  <div>
    <h2>Student Fee Calculator</h2>
    <p><strong>Student:</strong> {{ student.name }}</p>
    <p><strong>Course:</strong> {{ student.course }}</p>
    <p><strong>Tuition Fee:</strong> {{ student.tuitionFee }}</p>
    <p><strong>Amount Paid:</strong> {{ student.amountPaid }}</p>
    <p><strong>Balance:</strong> {{ balance }}</p>

    <button @click="payFiveThousand">Pay 5,000</button>
    <button @click="payTenThousand">Pay 10,000</button>
    <button @click="resetPayment">Reset Payment</button>
  </div>
</template>