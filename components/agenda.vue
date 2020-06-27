<template>
  <b-container>
    <h3>
      <b class="roboto-fat text-purple text-title">Agenda</b>
    </h3>
    <b-table
      hover
      bordered
      :items="items"
      :fields="fields"
      head-variant="light"
      class="mt-4"
    />
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      // Note `isActive` is left out and will not appear in the rendered table
      fields: ['first_name', 'last_name', 'age'],
      items: [
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' }
      ]
    }
  }
}
</script>
