<script setup>
import { ref } from 'vue'

import { useElementHover } from '@vueuse/core'

const hoveralbeButton = ref()
const isHovered = useElementHover(hoveralbeButton)
</script>

<template>
  <div id="experts" class="hero-section">
    <div class="view-wrapper flex gap-12 items-center justify-center flex-wrap">
      <div class="flex flex-col gap-8 flex-1 min-w-[300px]">
        <img src="@/assets/images/momentum-logo.svg" class="max-w-[200px]" />
        <span class="text-caption-l">Built by Momentum’s Healthcare experts: </span>
        <span class="text-left text-caption-m text-grey-dark"
          >At Momentum, we believe in elevating humanity through technology. Our work supports
          longevity and continuous life quality improvement by developing the most ingenious,
          cutting-edge solutions in healthcare. We're passionate about creating a world where no one
          feels helpless because of lack of access to medical information or diagnostics.</span
        >
        <span class="text-left text-caption-m text-grey-dark"
          >We combine deep healthcare expertise with technical excellence to deliver solutions that
          are secure, scalable, and compliant with industry standards like HIPAA, FHIR and GDPR.
        </span>
        <a
          ref="hoveralbeButton"
          href="https://www.themomentum.ai/"
          target="__blank"
          class="flex gap-2 items-center app-button app-button--text app-button--blue"
        >
          <button class="text-header-s--bold">Visit website</button>
          <i :class="{ arrow__right: isHovered }" class="pi pi-arrow-right arrow"></i>
        </a>
      </div>
      <div class="flex gap-4 column justify-center flex-wrap">
        <div class="linkedin-card">
          <img
            class="linkedin-card__avatar"
            src="@/assets/images/linkedin/piotr-sedzik.jpg"
            alt=""
          />
          <span class="text-header-xs--bold text-grey-dark">Piotr Sędzik</span>
          <span>CEO</span>
          <a href="https://www.linkedin.com/in/piotr-s%C4%99dzik-ba000b109/" target="_blank">
            <button>
              <i class="pi pi-linkedin text-xl text-grey linkedin-hover"></i>
            </button>
          </a>
        </div>
        <div class="linkedin-card">
          <img
            class="linkedin-card__avatar"
            src="@/assets/images/linkedin/piotr-sobusiak.jpg"
            alt=""
          />
          <span class="text-header-xs--bold text-grey-dark">Piotr Sobusiak</span>
          <span>CTO</span>
          <a href="https://www.linkedin.com/in/piotr-sobusiak-8a373b98/" target="_blank">
            <button>
              <i class="pi pi-linkedin text-xl text-grey linkedin-hover"></i>
            </button>
          </a>
        </div>
        <div class="linkedin-card">
          <img
            class="linkedin-card__avatar"
            src="@/assets/images/linkedin/jan-kaminski.jpg"
            alt=""
          />
          <span class="text-header-xs--bold text-grey-dark">Jan Kamiński</span>
          <span>CSO</span>
          <a href="https://www.linkedin.com/in/piotr-s%C4%99dzik-ba000b109/" target="_blank">
            <button>
              <i class="pi pi-linkedin text-lg text-xl text-grey linkedin-hover"></i>
            </button>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero-section {
  width: 100%;
  padding: 100px 36px;
  background: #f0f5fe;
}

.linkedin-card {
  background: var(--vt-c-white);
  border: 1px solid #dee8fc;
  border-radius: 12px;
  display: flex;
  padding: 24px;
  width: 180px;
  min-width: 180px;
  height: min-content;

  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: center;

  &__avatar {
    border-radius: 50%;
    width: 100px;
    min-width: 100px;
    height: 100px;
    min-height: 100px;
  }
}

.arrow {
  font-size: 14px;
  font-weight: 800;
  transition: transform 0.3s ease;

  &__right {
    transform: translateX(5px);
  }
}

.linkedin-hover {
  transition: color 0.3s ease;

  &:hover {
    color: var(--vt-c-blue);
  }
}
</style>
