<template>
  <div id="hero" class="hero-section">
    <div class="flex flex-col items-center justify-center gap-8 mb-16">
      <div class="flex flex-col items-center justify-center">
        <h1 class="text-header-3xl text-gradient text-center">Infrastructure as Code</h1>
      </div>
      <p class="text-header-m text-center">
        Launch your compliant, safe and secured app in seconds.
      </p>
      <a target="_blank" href="https://github.com/the-momentum/healthstack">
        <button class="app-button text-header-xs--bold">Check out our Open Source</button>
      </a>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero-section {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgb(255, 255, 255);
  background: linear-gradient(180deg, rgba(255, 255, 255, 1) 10%, rgb(198, 219, 254) 100%);

  @media screen and (max-width: 460px) {
    padding: 160px 24px;
  }
}
</style>
