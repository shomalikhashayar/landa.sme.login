<template>
  <div class="container" dir="ltr">
    <q-layout view="rHh rpR fFf" container style="height: 100vh">
      <TheSidebar />
      <q-page-container>
        <q-page>
          <router-view />
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script setup></script>

<style>
* {
  font-family: "Vazirmatn", sans-serif;
}
</style>
