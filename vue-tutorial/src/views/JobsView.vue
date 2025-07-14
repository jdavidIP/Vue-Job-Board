<script setup>
import JobListings from "@/components/JobListings.vue";
import { useRoute } from "vue-router";
import { useToast } from "vue-toastification";
import { onMounted } from "vue";

const route = useRoute();
const toast = useToast();

onMounted(() => {
  if (route.query.deleted === "true") {
    toast.success("Job deleted successfully.");
  }
});
</script>

<template>
  <JobListings />
</template>
