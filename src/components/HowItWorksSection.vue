<template>
  <div id="howItWorks" class="how-it-works-section">
    <div class="flex flex-col items-center justify-center gap-16">
      <h1 class="text-header-xl leading-10">How It Works</h1>

      <div class="card view-wrapper--extedned items-center flex-wrap">
        <div class="flex flex-col gap-12 column">
          <span class="text-header-m--bold"
            >On a quick setup video you can see why it reduces tedious ClickOps tasks, scales well,
            and is repeatable.
          </span>
          <span class="text-caption-m text-grey-dark"
            >Just display the S3 module, that creates S3 bucket on AWS with logging, versioning,
            encryption and private access. Then run a script, automatically you will create all
            elements of your infrastructure…and voila!
          </span>
        </div>
        <div class="card__video-container column h-max">
          <video controls>
            <source src="@/assets/videos/howItWorks.mov" type="video/mp4" />
          </video>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.how-it-works-section {
  width: 100%;
  padding: 64px 24px 128px 24px;
  background: var(--vt-c-white);
}

.column {
  flex: 1;
  min-width: 200px;
}

.card {
  background: rgb(224, 234, 252);
  background: linear-gradient(180deg, rgba(224, 234, 252, 1) 23%, rgba(249, 251, 254, 1) 100%);
  border: 1px solid #dee8fc;
  padding: 24px;
  border-radius: 12px;
  display: flex;
  gap: 64px;
  padding: 84px 64px;

  @media screen and (max-width: 460px) {
    flex-direction: column;
    gap: 32px;
    padding: 36px;
  }

  &__video-container {
    background-color: var(--vt-c-white);
    border-radius: 12px;
    max-width: 600px;
    width: 100%;
    overflow: hidden;
  }
}
</style>
