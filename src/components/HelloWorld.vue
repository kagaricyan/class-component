<template>
  <div class="hello">
    <h1>{{ username }}</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
interface User {
  name: string;
  email: string;
  phone: string;
}
@Component
export default class HelloWorld extends Vue {
  @Prop( { type: Object }) private user!: User

  localUser: User = this.user

  get username() {
    return this.localUser.name
  }
}
</script>
