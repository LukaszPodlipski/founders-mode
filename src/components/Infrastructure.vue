<template>
  <div id="infrastructure" class="infrastructure-section flex flex-col gap-24">
    <div class="view-wrapper flex flex-col items-center justify-center gap-8">
      <h2 class="text-header-xl leading-10 text-center">
        Quick infrastructure deployment for your applications
      </h2>
      <p class="text-header-s text-center text-grey">
        Healthstack provides thoroughly tested and well-maintained packages that deliver reliable
        and secure infrastructure without requiring extensive documentation review. It automatically
        generates resources and facilitates straightforward access to new infrastructure in a secure
        manner. It promotes efficient collaboration among developers and ensures seamless
        replication when deploying to production environments.
      </p>
    </div>
    <div class="flex gap-4 view-wrapper flex-wrap">
      <div class="card">
        <span class="text-header-s--bold">For HealthTech startups</span>
        <span class="text-caption-m text-grey-dark"
          >For healthtech startups racing to market, Healthstack eliminates the complexity of
          building compliant AWS infrastructure by providing battle-tested Terraform modules that
          are specifically designed for healthcare applications.
        </span>
      </div>
      <div class="card">
        <span class="text-header-s--bold">For Healthcare providers</span>
        <span class="text-caption-m text-grey-dark"
          >The tool offers healthcare providers a trusted way to deploy AWS infrastructure that's
          inherently HIPAA-compliant, eliminating the risk of breaches and compliance violations.
          Your IT team can use Healthstack's pre-built, security-hardened Terraform modules to
          rapidly deploy the services you need.
        </span>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.infrastructure-section {
  width: 100%;
  padding: 100px 36px 50px 36px;
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
  justify-content: start;
  flex-direction: column;
  flex: 1;
  min-width: 300px;

  @media screen and (max-width: 400px) {
    padding: 24px;
  }
}
</style>
