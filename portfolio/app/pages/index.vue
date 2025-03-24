<template>
  <div class="container">
    <aside>
      <Sidebar />
    </aside>
    <main>
      <Gallery />
    </main>
  </div>
</template>

<style>
.container {
  display: flex;
  width: 100vw;
  height: 100vh;
}

aside {
  width: 25%;
}
main {
  width: 75%;
}
</style>
