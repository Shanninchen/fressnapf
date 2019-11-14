<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex
        xs12
        mb-5
      >
        <h1 class="display-1 font-weight-bold mb-3">Overview of Starships in the SW Movies</h1>
        <v-layout justify-center>
          <v-simple-table
            fixed-header
            height="500"
          >
            <template v-slot:default>
              <thead>
              <tr>
                <th class="text-left">Name</th>
                <th class="text-left">Costs</th>
              </tr>
              </thead>
              <tbody>
              <tr v-for="ship in allStarships" :key="ship.name">
                <td class="text-left">{{ ship.name }}</td>
                <td class="text-left">{{ ship.costInCredits }}</td>
              </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import gql from 'graphql-tag';

export default {
  name: 'StarWars',
  apollo: {
    // Simple query that will update the 'hello' vue property
    allStarships: gql`query {
                   allStarships (orderBy: name_ASC) {
                    name,
                    costInCredits
                  }
                }`,
  },
};
</script>
