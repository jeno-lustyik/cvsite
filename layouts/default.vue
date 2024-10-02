<template>
  <div class="flex flex-col size-full">
    <header class="bg-gray-800 text-white p-4">
      <h1>My Nuxt App</h1>
    </header>

    <main class="flex-1 p-4">
      <slot /> <!-- This is where page content will be rendered -->
    </main>

    <footer class="bg-gray-200 p-4">
      <p>Footer content</p>
    </footer>
  </div>
</template>