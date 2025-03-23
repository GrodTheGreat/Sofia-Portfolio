<script setup>
const socials = [
  {
    name: "Behance",
    link: "https://www.behance.net/sofiaescobar_design",
    icon: "",
  },
  {
    name: "Instagram",
    link: "https://www.facebook.com/share/aBACSoiSTN/?mibextid=wwXlfr",
    icon: "",
  },
  {
    name: "Facebook",
    link: "https://www.facebook.com/share/aBACSoiSTN/?mibextid=wwXlfr",
    icon: "",
  },
  {
    name: "Email",
    link: "#",
    icon: "",
  },
];
</script>

<template>
  <div class="sidebar">
    <div class="logo">
      <img src="#" alt="Logo goes here" />
      <h2 class="name">Sofia<br />Escobar</h2>
    </div>
    <nav>
      <ul>
        <li>
          <a href="#">Illustration</a>
        </li>
        <li>
          <a href="#">Design</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
        <li>
          <a href="#">Contact</a>
        </li>
      </ul>
    </nav>
    <div class="socials">
      <ul class="socials-list">
        <li v-for="(social, index) in socials" :key="index">
          <a :href="social.link" target="_blank">
            {{ social.name }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: clamp(300px, 30%, 400px);
}

.logo {
  margin-top: 20%;
}

nav {
  margin-top: 10%;
}

.socials-list {
  display: flex;
  justify-content: center;
  gap: 16px;
  margin-top: 10%;
}

.name {
  color: rgb(219, 94, 72);
  font-weight: bold;
  font-size: 3rem;
}
</style>
