<template>
  <div>
    <UiPageHeader subject="執行役員および本部長" subheading="executive" />
    <article class="c-article">
      <div class="l-container--large l-container--contents">
        <div v-html="response.details.contents"></div>
      </div>
    </article>
  </div>
</template>

<script setup>
const config = useRuntimeConfig();

const { data: response } = await useFetch(
  `${config.public.kurocoApiDomain}/rcms-api/1/content/details/executive`,
  {
    server: false,
  }
);
</script>
