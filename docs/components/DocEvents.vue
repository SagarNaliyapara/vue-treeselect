<template>
  <table class="striped">
    <thead>
      <tr>
        <th>Name</th>
        <th>Attributes</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="event in events" :key="event.name">
        <td><strong>{{ event.name }}</strong></td>
        <td>{{ event.attributes }}</td>
        <td>{{ event.description }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
  export default {
    data: () => ({
      events: [ {
        name: 'open',
        attributes: '(id)',
        description: 'Emitted when the dropdown opens.',
      }, {
        name: 'close',
        attributes: '(value, id)',
        description: 'Emitted when the dropdown closes.',
      }, {
        name: 'input',
        attributes: '(value, id)',
        description: 'Emitted after value changes.',
      }, {
        name: 'search-change',
        attributes: '(searchQuery, id)',
        description: 'Emitted after the search query changes.',
      } ],
    }),
  }
</script>
