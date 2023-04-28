<template>
  <q-page class="row justify-center items-center">
    <q-header style="height: 80px" class="bg-white text-dark flex">
      <q-toolbar>
        <q-toolbar-title class="q-ml-md text-weight-bold"
          >Login</q-toolbar-title
        >
        <div class="flex q-pa-md q-gutter-sm">
          <q-btn
            unelevated
            no-caps
            color="blue-6"
            label="Sign up"
            class="text-weight-bold"
          />
          <q-btn-dropdown
            outline
            push
            no-caps
            icon="language"
            label="English"
            @click="onMainClick"
            class="text-dark shadow-1"
          >
            <q-list>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>Arabic</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>Farsi</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-btn-dropdown>
        </div>
      </q-toolbar>
    </q-header>
    <div class="column">
      <div class="logo flex justify-center">
        <q-img
          src="../assets/about-us-header.png"
          class="q-mb-md"
          style="width: 270px"
        />
      </div>
      <div class="row"></div>
      <div class="">
        <q-card class="no-shadow">
          <q-card-section>
            <q-form class="q-gutter-md">
              <q-input
                outlined
                v-model="ph"
                placeholder="Username (Mobile/Email) "
                dense
                class="text-body"
              />
              <q-input
                outlined
                v-model="ph"
                placeholder="Password"
                dense
                class="text-body"
              />
              <div class="row justify-between items-center">
                <div class="flex">
                  <q-btn
                    unelevated
                    color="grey-6"
                    label="65 + 8"
                    dense
                    class="q-px-md text-h6"
                  />
                </div>
                <div class="q-pr-md">
                  <q-btn round flat color="blue-6" icon="refresh" dense />
                </div>

                <div class="col-5">
                  <q-input
                    outlined
                    v-model="ph"
                    placeholder="1234"
                    dense
                    class="text-body"
                  />
                </div>
              </div>
            </q-form>
          </q-card-section>
          <q-card-actions class="q-px-md">
            <q-btn
              unelevated
              color="light-blue-6"
              size="md"
              class="full-width text-weight-bold"
              no-caps
              label="Log in"
              style="height: 40px"
            />
          </q-card-actions>
          <q-card-section class="text-center q-pa-none">
            <p class="forgot-password text-blue-7 q-mt-lg">
              <a href="#">Forgot your password?</a>
            </p>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");
</script>

<style>
.q-card {
  width: 300px;
}

.forgot-password a {
  text-decoration: none;
  color: #0087f6;
}
</style>
