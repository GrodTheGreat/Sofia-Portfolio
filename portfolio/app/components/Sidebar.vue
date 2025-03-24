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
  width: clamp(300px, 100%, 400px);
  height: 100vh;
  padding: 16px;
}

.logo {
  margin-top: 80%;
}

.name {
  letter-spacing: 0.1rem;
}

nav {
  margin-top: 20%;
}

nav li {
  padding: 8px;
}

nav a {
  text-decoration: none;
  color: black;
  font-size: 1.1rem;
  text-transform: uppercase;
}

.socials-list {
  display: flex;
  justify-content: center;
  gap: 16px;
  margin-top: 20%;
}

.name {
  color: rgb(219, 94, 72);
  font-weight: bold;
  font-size: 3rem;
}
</style>
