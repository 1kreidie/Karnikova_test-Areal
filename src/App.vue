<script>
import Records from './components/Records.vue';
  export default {
    components: { Records },
    data() {
      return {
        headers: [
            { content: 'ФИО', value: 'initials' },
            { content: 'Дата рождения', value: 'dateOfBirth' },
            { content: 'Серия/номер паспорта', value: 'passport' },
            { content: 'Контактная информация', value: 'contactInformation' },
            { content: 'Адрес проживания', value: 'residenceAddress' },
            { content: 'Отдел', value: 'department' },
            { content: 'Должность', value: 'jobTitle' },
            { content: 'Размер зарплаты', value: 'salaryAmount' },
            { content: 'Дата принятия на работу', value: 'hiringDate' },
            { content: '', value: 'actions' },
        ],
        infoRecords: [
          {
            initials: 'Калинина Ирина Викторовна',
            dateOfBirth: '30.03.1999',
            passport: '1222 213456',
            contactInformation: '+7999999',
            residenceAddress: 'г. Москва, ул. Октябрьская, д. 10, кв. 23',
            department: 'Закупки',
            jobTitle: 'Менеджер',
            salaryAmount: 10000,
            hiringDate: '12.04.2022'
          },
        ]
      }
    },
  }
</script>

<template>
  <section>
    <header class="head">
      <button>Создать сотрудника</button>
      <input type="text" placeholder="Найти сотрудника">
    </header>
    <table class="employeeRecords">
      <thead>
        <tr>
            <th v-for="head in headers" :key="head.value">{{ head.content }}</th>
        </tr>
      </thead>
      <tbody>
        <Records
          v-for="(info, i) in infoRecords"
          :key="i"
          :item="info"
          :headers="headers"
        />
    </tbody>
  </table>
  </section>
</template>



<style>
.head {
  display: flex;
  gap: 20px;
}

</style>