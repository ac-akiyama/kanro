<template>
  <div>
    <UiPageHeader subject="株式・株主情報" subheading="stock" />
    <article class="c-article">
      <div class="l-container--large l-container--contents">
        <a :href="response.details.ext_1.url" target="_blank">PDFを開く</a>
      </div>
    </article>
  </div>
</template>

<script setup>
const config = useRuntimeConfig();

const { data: response } = await useFetch(
  `${config.public.kurocoApiDomain}/rcms-api/4/pdf/stock`,
  {
    credentials: 'include',
  }
);
</script>
