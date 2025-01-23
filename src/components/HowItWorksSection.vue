<template>
  <div id="howItWorks" class="how-it-works-section">
    <div class="flex flex-col items-center justify-center gap-16">
      <h1 class="text-header-xl leading-10">How It Works</h1>

      <div class="card view-wrapper--extedned items-center flex-wrap">
        <div class="flex flex-col gap-12 column">
          <span class="text-header-m--bold"
            >In a quick setup video, you’ll see how it reduces tedious ClickOps tasks, scales
            efficiently, and ensures repeatability.
          </span>
          <span class="text-caption-m text-grey-dark"
            >Simply showcase the S3 module, which creates an S3 bucket on AWS with logging,
            versioning, encryption, and private access. Then, run a script to automatically create
            all elements of your infrastructure… and voilà!
          </span>
        </div>
        <div class="card__video-container column h-max">
          <video controls>
            <source src="@/assets/videos/howItWorks.mov#t=0.1" type="video/mp4" />
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

    // min-height: 348px;
    // height: auto !important;
  }
}
</style>
