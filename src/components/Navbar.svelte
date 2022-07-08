<script lang="ts">
  import { Language } from "../types";
  let active = "about";
</script>

<nav class="py-8 flex items-center gap-4 w-full text-zinc-600">
  <a href="/">
    <span class="text-black text-4xl font-serif font-medium m-4">
      Web Mesh
    </span>
  </a>
  <span class="hidden lg:flex gap-4">
    <div class:active={active == "about"}>
      <a href="/#about">O náš</a>
    </div>

    <div class:active={active == "portfolio"}>
      <a href="/#portfolio">Portfolio</a>
    </div>
    <div class:active={active == "contact"}>
      <a href="/#contact">Kontakt</a>
    </div>
    <div class:active={active == "team"}>
      <a href="/#team">Náš tým</a>
    </div>
  </span>
  <span class="flex-grow" />
  <a
    href="mailto:strankylouny@gmail.com"
    class="font-bold hover:text-black duration-300 text-zinc-600"
    >strankylouny@gmail.com</a
  >
</nav>

<style>
  .active {
    color: #000;
  }

  div {
    position: relative;
    transition-duration: 300ms;
    font-weight: 700;
    @apply text-zinc-600;
  }

  div:hover {
    color: #000;
  }

  div:hover:before,
  .active:before {
    position: absolute;
    content: "";
    position: absolute;
    width: 50%;
    left: 0;
    right: 0;
    margin-left: auto;
    margin-right: auto;
    height: 4px;
    bottom: -2px;
    border-bottom: 2px solid #000;
  }

  div:before {
    position: absolute;
    content: "";
    position: absolute;
    width: 25%;
    left: 0;
    right: 0;
    margin-left: auto;
    margin-right: auto;
    height: 4px;
    bottom: -5px;
    border-bottom: 2px solid transparent;
    transition-duration: 300ms;
  }
</style>
