<template>
  <div>
    <UiPageHeader subject="IR情報" subheading="ir" />
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
  `${config.public.kurocoApiDomain}/rcms-api/4/pdf/ir`,
  {
    credentials: 'include',
  }
);
</script>
