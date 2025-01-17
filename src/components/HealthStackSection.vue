<template>
  <div id="healthStack" class="hero-section flex flex-col gap-36">
    <div class="flex gap-24 justify-between flex-wrap">
      <div class="flex flex-col items-start justify-center gap-8 max-w-[600px] column center">
        <h2 class="text-header-2xl leading-10 text-left">What is HeathStack?</h2>
        <p class="text-header-m text-left">
          While it’s easy to manually provision a single server, as your application and business
          scale, it requires a lot of repetitive work that can be reduced
        </p>
        <p class="text-header-m--bold-strong text-left">
          Healthstack was created to make infrastructure provisioning efficient, tested, and
          reliable for your application. Simply include the module (we are open source), input your
          parameters, apply, and you’re ready to build. It’s that simple.
        </p>
      </div>
      <div class="max-w-[576px] column center">
        <img src="@/assets/images/image1.jpg" class="rounded-3xl w-full h-auto block" />
      </div>
    </div>
    <div class="flex gap-24 justify-between flex-wrap-reverse">
      <div class="max-w-[576px] column center">
        <img src="@/assets/images/image2.jpg" class="rounded-3xl w-full h-auto block" />
      </div>
      <div class="flex flex-col items-start justify-center gap-8 max-w-[600px] column center">
        <h2 class="text-header-2xl leading-10 text-left">Why Open Source?</h2>
        <p class="text-header-m text-left">
          When using SaaS solutions, compliance features are typically limited to enterprise pricing
          tiers, which can be cost-prohibitive at the beginning of your business journey. We want to
          keep Healthstack community-driven, tested, and open-source to find the sweet spot between
          easy, fast, and compliant deployment while maintaining reasonable pricing.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero-section {
  width: 100%;
  padding: 140px 36px;
  background: linear-gradient(180deg, rgba(255, 255, 255, 1) 60%, rgba(98, 169, 240, 0.298) 100%);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.column {
  flex: 1;
  min-width: 300px;
}
</style>
