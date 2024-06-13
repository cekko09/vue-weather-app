<template>
  <div>
    <Suspense>
      <AsyncCityView />
      <template #fallback> 
        <CityViewSkeleton/>
      </template>
    </Suspense>
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";
import axios from "axios";
import { ref } from "vue";
import AsyncCityView from "../components/AsyncCityView.vue";
import CityViewSkeleton from "../components/CityViewSkeleton.vue";

const route = useRoute();
</script>
