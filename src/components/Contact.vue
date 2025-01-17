<script setup>
import { ref } from 'vue'

const email = ref('')
const message = ref('')
</script>

<template>
  <div id="contact" class="contact-section flex flex-col gap-24">
    <div class="view-wrapper flex flex-col items-center justify-center gap-8">
      <h2 class="text-header-xl leading-10 text-center">Need more info about CompliantChatGPT?</h2>
      <p class="text-header-s text-center text-grey">
        Leave us your message and we’ll get back to you!
      </p>
    </div>
    <div class="view-wrapper flex flex-col items-center">
      <form class="flex gap-4 flex-col items-center w-full max-w-[500px]" action="">
        <label for="email" class="w-full">Email</label>
        <input
          id="email"
          name="email"
          class="input"
          type="text"
          v-model="email"
          placeholder="Your email here"
        />
        <label for="message" class="w-full mt-6">Message</label>
        <textarea
          id="message"
          name="message"
          class="input input--textarea"
          type="text"
          v-model="message"
          rows="6"
          placeholder="Your message here"
        />
        <button type="submit" class="app-button app-button--md w-full mt-4">Submit</button>
      </form>
    </div>
  </div>
</template>

<style scoped lang="scss">
.contact-section {
  width: 100%;
  padding: 100px 24px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: rgb(255, 255, 255);
  background: linear-gradient(180deg, rgba(255, 255, 255, 1) 10%, rgba(222, 233, 252, 1) 100%);
}

.card {
  background: var(--vt-c-white);
  border: 1px solid #dee8fc;
  border-radius: 12px;
  display: flex;
  padding: 48px;
  width: 100%;
  gap: 24px;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.input {
  border: 2px solid transparent;
  width: 100%;
  height: 2.5em;
  padding-left: 0.8em;
  outline: none;
  overflow: hidden;
  background-color: #ffffff;
  border-radius: 10px;
  transition: all 0.5s;

  &--textarea {
    height: 100px;
    padding: 12px;
  }
}

.input:hover,
.input:focus {
  border: 2px solid #4a9dec;
  box-shadow: 0px 0px 0px 7px rgb(74, 157, 236, 20%);
  background-color: white;
}
</style>
