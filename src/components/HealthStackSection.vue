<script setup>
import { ref } from 'vue'
import VCodeBlock from '@wdns/vue-code-block'
const code = ref(`module "vpn" {
  source = "github.com/the-momentum/
    healthstack.git//aws-vpn/module"

  organization_name   = "Momentum"
  vpn_domain          = "vpn.myvpn.com"
  vpc_id              = "vpc-123123"
  subnet_ids          = [
    "subnet-123123",
    "subnet-456456",
  ]

  client_cidr_block   = "10.100.0.0/22"
  target_network_cidr = "172.31.0.0/16"

  tags = {
    Environment = "test"
  }
}`)
</script>

<template>
  <div id="healthStack" class="hero-section flex flex-col gap-36">
    <div class="flex gap-24 justify-between flex-wrap">
      <div class="flex flex-col items-start justify-center gap-8 max-w-[600px] column center">
        <h2 class="code-column-text text-header-2xl leading-10 text-left">What is HealthStack?</h2>
        <p class="code-column-text text-header-m text-left">
          While manually provisioning a single server is simple, scaling your application and
          business can lead to repetitive and time-consuming tasks.
        </p>
        <p class="code-column-text text-header-m--bold-strong text-left">
          Healthstack was created to make infrastructure provisioning efficient, tested, and
          reliable for your application. Just include the module (we’re open source), input your
          parameters, apply, and you’re ready to build. It’s that simple.
        </p>
      </div>
      <div class="code-column-block column center">
        <VCodeBlock :code="code" highlightjs lang="javascript" theme="neon-bunny" />
      </div>
    </div>
    <div class="flex gap-24 justify-between flex-wrap-reverse">
      <div class="max-w-[576px] center">
        <img src="@/assets/images/image1.jpg" class="rounded-3xl w-full h-auto block" />
      </div>
      <div class="flex flex-col items-start justify-center gap-8 max-w-[600px] column center">
        <h2 class="text-header-2xl leading-10 text-left">Why Open Source?</h2>
        <sp class="text-header-m text-left">
          When using SaaS solutions, compliance features are typically limited to enterprise pricing
          tiers, which can be cost-prohibitive at the beginning of your business journey. We want to
          keep Healthstack community-driven, tested, and open-source to find the sweet spot between
          easy, fast, and compliant deployment while maintaining reasonable pricing.
        </sp>
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

  @media screen and (max-width: 460px) {
    min-width: 200px;
  }
}

.code-column-block {
  max-width: 576px;

  @media screen and (max-width: 860px) {
    max-width: 90%;
  }
}

.code-column-text {
  // VCodeBlock behaves strangely on small mobile screens
  @media screen and (max-width: 860px) {
    padding: 0 20px;
  }
}
</style>
