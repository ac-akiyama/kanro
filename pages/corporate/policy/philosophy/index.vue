<template>
  <div>
    <UiPageHeader subject="企業行動憲章" subheading="philosophy" />
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
  `${config.public.kurocoApiDomain}/rcms-api/1/content/details/philosophy`,
  {
    server: false,
  }
);
</script>
