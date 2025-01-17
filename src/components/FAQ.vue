<script setup>
import { ref } from 'vue'

const faqItems = ref([
  {
    question: 'What is Healthstack?',
    answer:
      "It's a repository of Terraform modules designed to provide secure and compliant infrastructure on AWS.",
    collapsed: true,
  },
  {
    question: 'Is this solution free?',
    answer: "Yes, it's always free, but you will need to pay for the AWS resources you use.",
    collapsed: true,
  },
  {
    question: 'Is this solution compliant?',
    answer:
      " Yes, but please note that compliance is a broad topic that also includes your company's internal processes and measures taken to protect your infrastructure. With Healthstack, you'll be using AWS-managed, compliant services. For more information, please check the documentation here:   <a class='text-blue' href='https://aws.amazon.com/compliance/hipaa-eligible-services-reference/' target='__blank'>https://aws.amazon.com/compliance/hipaa-eligible-services-reference/</a>",
    collapsed: true,
  },
  {
    question: 'What if I need a custom feature or service?',
    answer: 'Contact us or feel free to contribute on GitHub.',
    collapsed: true,
  },
])
</script>

<template>
  <div id="faq" class="faq-section flex flex-col gap-24">
    <div class="view-wrapper flex flex-col items-center justify-center gap-8">
      <h2 class="text-header-xl leading-10 text-center">Frequently Asked Questions</h2>
      <p class="text-header-s text-center text-grey">
        Explore the answers to common queries and make the most of your Healthstack experience.
      </p>
    </div>
    <div class="flex flex-col view-wrapper">
      <button
        v-for="(item, idx) in faqItems"
        :key="idx"
        class="faq-item"
        :class="{ 'faq-item--border': idx !== faqItems.length - 1 }"
        @click="item.collapsed = !item.collapsed"
      >
        <div class="flex w-full justify-between">
          <span class="text-caption-m--bold text-left">{{ item.question }}</span>
          <i class="pi text-xs font-bold" :class="[item.collapsed ? 'pi-plus' : 'pi-minus']"></i>
        </div>
        <span
          v-if="!item.collapsed"
          v-html="item.answer"
          class="text-header-xs text-left text-grey"
        />
      </button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.faq-section {
  width: 100%;
  padding: 100px 36px;
  background: var(--vt-c-white);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.faq-item {
  display: flex;
  flex-direction: column;
  width: 100%;
  gap: 12px;
  padding: 24px 0;

  &--border {
    border-bottom: 1px solid var(--vt-c-blue-light);
  }
}
</style>
