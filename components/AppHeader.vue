<template>
  <header class="l-header" :class="{ 'is-open': Drawer }">
    <div class="l-header__inner">
      <div class="l-header__logo">
        <NuxtLink to="/" @click.native="Drawer = false"
          ><img src="~/assets/image/logo.svg" alt="Company Name" />
        </NuxtLink>
      </div>
      <nav class="l-header__nav">
        <button
          @click="Drawer = !Drawer"
          type="button"
          class="l-header__nav__toggle"
        >
          <div class="l-header__nav__toggle__icon">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </button>
        <div class="l-header__nav__inner">
          <ul class="l-header__nav__list">
            <li class="l-header__nav__list__item">
              <NuxtLink to="/corporate/" @click.native="Drawer = false"
                >会社情報</NuxtLink
              >
            </li>
            <li class="l-header__nav__list__item">
              <NuxtLink to="/ir/" @click.native="Drawer = false"
                >IR情報</NuxtLink
              >
            </li>
            <li class="l-header__nav__list__item">
              <NuxtLink to="/csr/" @click.native="Drawer = false"
                >サステナビリティ</NuxtLink
              >
            </li>
            <li class="l-header__nav__list__item">
              <NuxtLink to="/RandD/" @click.native="Drawer = false"
                >カンロの研究と技術</NuxtLink
              >
            </li>
            <li class="l-header__nav__list__item">
              <NuxtLink to="/contact/" @click.native="Drawer = false"
                >採用情報</NuxtLink
              >
            </li>
            <li class="l-header__nav__list__item">
              <NuxtLink to="/contact/" @click.native="Drawer = false"
                >お客様サポート</NuxtLink
              >
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { computed, ref } from 'vue';
const Drawer = ref(false);
const { authUser, isLoggedIn, logout } = useAuth();
</script>
