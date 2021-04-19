<template>
  <article>
    <p>{{ greeting }}</p>
    <p>
      {{ `My name is ${name}. I'm ${age} years old.` }}
    </p>
    <button class="btn" @click="onClickQuestion">Where are you from?</button>
    <p>{{ country }}</p>
  </article>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class sample extends Vue {
  public greeting: string = 'Hello!!'
  public name: string = 'mican'
  public age: number = 23
  public country: string = ''

  public onClickQuestion() {
    this.country = 'I was born in Tokyo.'
  }
}
</script>

<style scoped>
.btn {
  padding: 4px 16px;
  color: #333;
  background-color: azure;
  border-radius: 8px;
}
</style>
