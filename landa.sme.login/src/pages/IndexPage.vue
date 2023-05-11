<!-- <template>
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
</style> -->
<template>
  <q-page class="row justify-center items-center bg-blue-1">
    <q-header class="bg-white text-black q-qx-md">
      <q-toolbar class="q-px-lg">
        <q-toolbar-title class="text-black"
          ><a href="#" class="navbar-logo">Landa-SME</a></q-toolbar-title
        >

        <div class="flex items-center q-gutter-sm cursor-pointer">
          <div class="text-body">خشایار</div>
          <q-icon color="dark" size="sm" name="o_account_circle" />
          <q-menu>
          <q-list dense padding style="min-width: 240px">
            <q-item-label class="text-h5" header>
              <q-avatar color="blue-4" class="q-mx-sm" text-color="white">A</q-avatar>
              خشایار
            </q-item-label>
            <q-item clickable v-close-popup>
              <q-item-section avatar>
                <q-avatar icon="password" />
              </q-item-section>
              <q-item-section>
                <q-item-label>change password</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup tabindex="0">
              <q-item-section avatar>
                <q-avatar icon="logout" />
              </q-item-section>
              <q-item-section>
                <q-item-label>logout</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-menu>
        </div>
      </q-toolbar>
    </q-header>

    <q-footer bordered class="bg-white text-dark q-py-md xs">
      <div class="q-pb-sm" v-if="showMoreOptions">
        <q-item clickable v-ripple class="q-py-sm">
          <q-item-section avatar>
            <q-avatar
              color="grey-4"
              text-color="dark"
              icon="o_person"
              size="md"
            />
          </q-item-section>
          <q-item-section>Entering the Business</q-item-section>
        </q-item>
        <q-item clickable v-ripple class="q-py-sm">
          <q-item-section avatar class="q-py-md">
            <q-avatar
              color="grey-4"
              text-color="dark"
              icon="o_person_add"
              size="md"
            />
          </q-item-section>
          <q-item-section>Invite User</q-item-section>
        </q-item>
        <q-item clickable v-ripple class="q-py-sm">
          <q-item-section avatar>
            <q-avatar
              color="grey-4"
              text-color="dark"
              icon="o_delete"
              size="md"
            />
          </q-item-section>
          <q-item-section>Delete</q-item-section>
        </q-item>
        <q-item clickable v-ripple class="q-py-sm">
          <q-item-section avatar>
            <q-avatar
              color="grey-4"
              text-color="dark"
              icon="credit_card"
              size="md"
            />
          </q-item-section>
          <q-item-section>Invite User</q-item-section>
        </q-item>
      </div>
      <div class="flex justify-between items-center q-pl-sm q-pr-lg">
        <div class="col-2">
          <q-btn
            class="more-icon"
            style="color: grey"
            key="more-button"
            unelevated
            falt
            round
            :ripple="false"
            icon="more_vert"
            size="md"
            @click="showMoreOptions = !showMoreOptions"
          >
          </q-btn>
        </div>
        <div class="flex q-gutter-sm col-2">
          <q-chip
            class="chips expire-date"
            square
            icon="o_history"
            :ripple="false"
            style="font-size: 12px; background-color: #ffe1b4"
            >1402/08/09</q-chip
          >
          <div class="col-2">
            <q-btn
              class="service-extension"
              unelevated
              color="orange"
              icon="o_shopping_bag"
              size="sm"
            />
          </div>
        </div>
      </div>
    </q-footer>

    <!-- Mobile View -->
    <div class="q-pa-md items-start q-gutter-md xs q-mt-sm q-mb-lg">
      <q-card class="select-business-card-mobile q-card-mobile" bordered>
        <q-item class="q-px-lg q-py-lg">
          <q-item-section>
            <q-item-label
              class="text-weight-bold text-grey-10"
              style="font-size: 18px"
              >My Businesses</q-item-label
            >
            <q-item-label
              class="text-body text-grey-7 q-pr-lg"
              caption
              style="font-size: 13px"
            >
              Click on the business name to enter
            </q-item-label>
          </q-item-section>
          <div class="flex items-center q-gutter-md">
            <q-icon color="grey" size="md" name="o_help_outline" />
            <q-btn unelevated round color="green-7" icon="add">
              <q-tooltip anchor="top right" self="top left">
                Add New Business
              </q-tooltip>
            </q-btn>
          </div>
        </q-item>

        <q-separator />
        <q-card-section class="q-pa-lg q-gutter-md">
          <q-card
            class="row selectable my-inner-card row justify-start q-px-md items-center no-shadow"
            bordered
          >
            <div class="icon flex items-center q-gutter-md">
              <div class="">
                <q-avatar
                  color="grey-4"
                  text-color="dark"
                  icon="o_person_add"
                  size="lg"
                />
              </div>

              <div class="business-button">
                <q-btn
                  class="business-name"
                  flat
                  no-caps
                  text-color="dark"
                  :ripple="{ color: 'grey-6' }"
                >
                  <div class="text-weight-bold" style="font-size: 12px">
                    دومان سامانه برای تست
                  </div>
                  <q-icon right size="xs" name="o_login" />
                </q-btn>
              </div>
            </div>
          </q-card>

          <q-card
            class="selectable my-inner-card row justify-start q-px-md items-center no-shadow"
            bordered
          >
            <div class="icon flex items-center q-gutter-md">
              <div class="">
                <q-avatar
                  color="grey-4"
                  text-color="dark"
                  icon="o_person"
                  size="lg"
                />
              </div>

              <div class="business-button">
                <q-btn
                  class="business-name"
                  flat
                  no-caps
                  text-color="dark"
                  :ripple="{ color: 'grey-6' }"
                >
                  <div class="text-weight-bold" style="font-size: 12px">
                    دفتر کارگشا (دمو)
                  </div>
                  <q-icon right size="xs" name="o_login" />
                </q-btn>
              </div>
            </div>
          </q-card>
        </q-card-section>
      </q-card>
    </div>

    <!-- Desktop View -->
    <div class="q-pa-md q-mt-md q-mb-xl row items-start q-gutter-md md">
      <q-card class="select-business-card q-card-desktop" bordered>
        <q-item class="q-px-lg q-py-lg">
          <q-item-section>
            <q-item-label
              class="text-weight-bold text-grey-10"
              style="font-size: 18px"
              >My Businesses</q-item-label
            >
            <q-item-label
              class="text-body text-grey-7"
              caption
              style="font-size: 13px"
            >
              Click on the business name to enter
            </q-item-label>
          </q-item-section>
          <div class="flex items-center q-gutter-md">
            <q-icon color="grey" size="md" name="o_help_outline" />
            <q-btn unelevated round color="green-7" icon="add">
              <q-tooltip anchor="top right" self="top left">
                Add New Business
              </q-tooltip>
            </q-btn>
          </div>
        </q-item>

        <q-separator />
        <q-card-section class="q-pa-lg q-gutter-md">
          <q-card
            class="selectable my-inner-card row justify-around items-center no-shadow q-pl-sm"
            bordered
          >
            <div class="icon flex items-center q-gutter-md col-6">
              <q-avatar
                color="grey-4"
                text-color="dark"
                icon="o_person_add"
                size="lg"
              />

              <q-btn
                class="business-name"
                flat
                no-caps
                text-color="dark"
                :ripple="{ color: 'grey-6' }"
              >
                <div class="text-weight-bold" style="font-size: 12px">
                  دومان سامانه برای تست
                </div>
                <q-icon right size="xs" name="o_login" />
              </q-btn>
            </div>

            <div class="flex items-center q-gutter-xs col-4 q-pl-md">
              <div class="">
                <q-chip
                  class="chips expire-date flex items-center"
                  square
                  icon="o_history"
                  :ripple="false"
                  style="font-size: 12px; background-color: #ffe1b4"
                  >1402/08/09</q-chip
                >
              </div>
              <div class="">
                <q-btn
                  class="service-extension"
                  unelevated
                  color="orange"
                  icon="o_shopping_bag"
                  size="sm"
                />
              </div>
            </div>
            <div class="more-options col-1 q-pl-xs">
              <q-btn
                class="more-icon"
                style="color: grey"
                unelevated
                falt
                round
                :ripple="false"
                icon="more_vert"
                size="md"
              />
              <q-menu>
                <q-list style="min-width: 100px">
                  <q-item clickable v-close-popup>
                    <q-item-section>
                      <div class="flex items-center q-gutter-sm">
                        <q-avatar
                          color="grey-4"
                          text-color="dark"
                          icon="login"
                          size="sm"
                        />
                        <div class="text-body" style="font-size: 12px">
                          Entering the Business
                        </div>
                      </div>
                    </q-item-section>
                  </q-item>
                  <q-item clickable v-close-popup>
                    <q-item-section
                      ><div class="flex items-center q-gutter-sm">
                        <q-avatar
                          color="grey-4"
                          text-color="dark"
                          icon="o_person_add"
                          size="sm"
                        />
                        <div class="text-body" style="font-size: 12px">
                          Invite User
                        </div>
                      </div></q-item-section
                    >
                  </q-item>
                  <q-separator />
                  <q-item clickable v-close-popup>
                    <q-item-section>
                      <div class="flex items-center q-gutter-sm">
                        <q-avatar
                          color="grey-4"
                          text-color="dark"
                          icon="o_delete"
                          size="sm"
                        />
                        <div class="text-body" style="font-size: 12px">
                          Delete
                        </div>
                      </div>
                    </q-item-section>
                  </q-item>
                  <q-separator />
                  <q-item clickable v-close-popup>
                    <q-item-section>
                      <div class="flex items-center q-gutter-sm">
                        <q-avatar
                          color="grey-4"
                          text-color="dark"
                          icon="credit_card"
                          size="sm"
                        />
                        <div class="text-body" style="font-size: 12px">
                          Payment History
                        </div>
                      </div>
                    </q-item-section>
                  </q-item>
                </q-list>
              </q-menu>
            </div>
          </q-card>

          <q-card
            class="selectable my-inner-card row justify-around items-center no-shadow q-pl-sm"
            bordered

          >
            <div class="icon flex items-center q-gutter-md col-6">
              <div class="">
                <q-avatar
                  color="grey-4"
                  text-color="dark"
                  icon="o_person"
                  size="lg"
                />
              </div>

              <div class="">
                <q-btn
                  class="business-name"
                  flat
                  no-caps
                  text-color="dark"
                  :ripple="{ color: 'grey-6' }"
                >
                  <div class="text-weight-bold" style="font-size: 12px">
                    دفتر کارگشا (دمو)
                  </div>
                  <q-icon right size="xs" name="o_login" />
                </q-btn>
              </div>
            </div>

            <div class="flex items-center q-gutter-xs col-4 q-pl-md">
              <div class="">
                <q-chip
                  class="chips expire-date flex items-center"
                  square
                  icon="o_history"
                  :ripple="false"
                  style="font-size: 12px; background-color: #ffe1b4"
                  >1402/08/09</q-chip
                >
              </div>
            </div>
            <div class="more-options col-1 q-pl-xs">
              <q-btn
                class="more-icon"
                style="color: grey"
                unelevated
                falt
                :ripple="false"
                round
                icon="more_vert"
                size="md"
              />
              <q-menu>
                <q-list style="min-width: 100px">
                  <q-item clickable v-close-popup>
                    <q-item-section>
                      <div class="flex items-center q-gutter-sm">
                        <q-avatar
                          color="grey-4"
                          text-color="dark"
                          icon="login"
                          size="sm"
                        />
                        <div class="text-body" style="font-size: 12px">
                          Entering the Business
                        </div>
                      </div>
                    </q-item-section>
                  </q-item>
                </q-list>
              </q-menu>
            </div>
          </q-card>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<style>
.q-toolbar__title {
  font-size: 14px;
  font-weight: 600;
}

.q-card-desktop {
  width: 620px;
}

.q-card-mobile {
  width: 320px;
}

.select-business-card {
  border-radius: 10px;
  box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.2);
}

.select-business-card-mobile {
  border-radius: 10px;
  box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.2);
}

.my-inner-card {
  width: auto;
  height: 90px;
  border-radius: 5px;
}

.business-name {
  border-radius: 5px;
  padding: 8px 12px;
  border: 1px solid rgb(230, 230, 230);
}

.chips {
  padding: 21px 15px;
}

.service-extension {
  padding: 12px 12px;
  border-radius: 5px;
}

.q-btn .q-focus-helper {
  display: none;
}

.selectable {
  cursor: pointer;
}

.card-selection {
  border: 1.5px solid #2196f3;
}

.navbar-logo {
  text-decoration: none;
  color: black;
}

.more-icon {
  margin-left: 2px;
}
</style>

<script setup>
import { ref } from "vue";

const showMoreOptions = ref(false);

const cardSelected = ref(false)

const cardSelection = () =>{
  this.cardSelected = !this.cardSelected

}



</script>
