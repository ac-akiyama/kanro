<template>
  <div>
    <UiPageHeader subject="電子公告" subheading="publicnotice" />
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
  `${config.public.kurocoApiDomain}/rcms-api/4/pdf/publicnotice`,
  {
    credentials: 'include',
  }
);
</script>
