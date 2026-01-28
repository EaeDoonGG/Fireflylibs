<template>
  <div class="error-page">
    <div class="error-card">
      <span class="badge">404</span>
      <h1>Looks like you got lost</h1>
      <p>
        The page you are looking for does not exist.<br />
        This path leads nowhere.
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{ error: { statusCode?: number } | null }>();
</script>