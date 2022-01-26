<template>
  <div class="home">
    <HelloWorld :user="user" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {
  user = { name: '张三', email: '1@1.com', phone: '13212341234' };
}
</script>
