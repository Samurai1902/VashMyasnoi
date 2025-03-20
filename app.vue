<template>
  <div class="app-wrapper">
      <n-config-provider :theme-overrides="themeOverrides" :locale="ruRU" :date-locale="dateRuRU">
          <n-message-provider>
              <n-notification-provider placement="bottom-right">
                  <n-dialog-provider>
                      <NuxtLayout>
                          <NuxtPage />
                      </NuxtLayout>
                  </n-dialog-provider>
              </n-notification-provider>
          </n-message-provider>
      </n-config-provider>
  </div>
</template>

<script setup>
import {
  ruRU,
  dateRuRU,
  NConfigProvider,
  NMessageProvider,
  NNotificationProvider,
  NDialogProvider,
} from "naive-ui";
const themeOverrides = {};
</script>

<style src="~/assets/css/root.css" />
<style src="~/assets/css/fonts.css" />
<style src="~/assets/css/main.css" />
