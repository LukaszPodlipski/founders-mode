<template>
  <div id="contact" class="contact-section flex flex-col gap-24">
    <div class="view-wrapper flex flex-col items-center justify-center gap-8">
      <h2 class="text-header-xl leading-10 text-center">Need more info about CompliantChatGPT?</h2>
      <p class="text-header-s text-center text-grey">
        Leave us your message and we’ll get back to you!
      </p>
    </div>
    <div class="flex gap-4 view-wrapper">form</div>
  </div>
</template>

<style scoped lang="scss">
.contact-section {
  width: 100%;
  padding: 100px 24px;
  background: var(--vt-c-white);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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
</style>
