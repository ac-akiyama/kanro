<template>
  <div>
    <UiPageHeader subject="株主総会" subheading="meeting" />
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
  `${config.public.kurocoApiDomain}/rcms-api/4/pdf/meeting`,
  {
    credentials: 'include',
  }
);
</script>
