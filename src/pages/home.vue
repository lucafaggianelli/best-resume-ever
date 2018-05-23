<template>
<v-layout row wrap justify-center>
  <v-card>
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex xs4>
          <v-text-field
              v-model="person.name.first"
              label="First Name">
          </v-text-field>
        </v-flex>
        <v-flex xs4>
          <v-text-field
              v-model="person.name.middle"
              label="Middle">
          </v-text-field>
        </v-flex>
        <v-flex xs4>
          <v-text-field
              v-model="person.name.last"
              label="Last Name">
          </v-text-field>
        </v-flex>
      </v-layout>
    </v-container>
    <v-card-actions>
      <v-btn color="primary">Save</v-btn>
    </v-card-actions>
  </v-card>
</v-layout>
</template>

<script>
import yaml from 'js-yaml';
import { PERSON } from '../../resume/data.yml';

export default {
  data () {
    return {
      person: yaml.load(PERSON)
    };
  }
};
</script>

<style>

</style>
