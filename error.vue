<template>
  <div class="error-page">
    <div class="error-card">
      <span class="badge">404</span>
      <h1>You seem to be lost</h1>
      <p>
        The page you’re looking for doesn’t exist.<br />
        This path leads nowhere.
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{ error: { statusCode?: number } | null }>();
</script>
