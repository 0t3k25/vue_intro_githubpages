<template>
  <v-card width="80%" height="auto" class="rounded-xl mx-auto">
    <v-row no-gutters align-content="center">
      <v-col>
        <v-img src="/my-face.png" class="my-5 my-face rounded-circle"> </v-img>
      </v-col>
      <v-col class="py-5">
        <h3>{{ profile.myName }}</h3>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>趣味:{{ profile.hobby }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title
                >出身国:{{ profile.country }}</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'nuxt-property-decorator'

@Component
export default class FaceLogo extends Vue {
  @Prop(Object) readonly profile: any
}
</script>

<style>
.my-face {
  width: 200px;
}
</style>
