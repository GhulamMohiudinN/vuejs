<script setup lang="ts">
import Show from "@/assets/vueJs/view.png";
import Hide from "@/assets/vueJs/hide.png";
import { useRouter } from "vue-router";

const router = useRouter();

const redirectToCompany = () => {
  router.push({ name: "company" });
};

let a: boolean = false;

function pass() {
  const passwordInput = document.getElementById("password") as HTMLInputElement;
  const passIcon = document.getElementById("pass-icon") as HTMLImageElement;
  if (passwordInput && passIcon) {
    if (a) {
      passwordInput.type = "password";
      passIcon.src = Hide;
      a = false;
    } else {
      passwordInput.type = "text";
      passIcon.src = Show;
      a = true;
    }
  }
}
</script>

<template>
  <div
    class="bg-[url('@/assets/vueJs/Background.png')] bg-cover h-screen bg-no-repeat text-white"
  >
    <div class="w-fit mx-auto pt-35">
      <img class="w-70 sm:w-90" src="@/assets/vueJs/Logo.png" alt="" />
    </div>
    <div
      class="border-2 border-black bg-white text-blackLight mt-16 w-60 sm:w-235 mx-auto rounded-[40px]"
    >
      <div>
        <p class="font-light text-textGrey text-4xl text-center py-6">
          Bienvenido
        </p>
        <input
          class="border-b border-lightGrey ml-6 pl-1.5 outline-none text-xl w-[80%] mb-4 sm:mb-7.5"
          type="text"
          placeholder="usuario"
        />
        <input
          class="border-b border-lightGrey ml-6 pl-1.5 outline-none text-xl w-[80%]"
          type="password"
          id="password"
          placeholder="contrasena"
        />
        <img
          src="@/assets/vueJs/hide.png"
          @click="pass"
          class="relative ml-[80%] -mt-5 cursor-pointer"
          id="pass-icon"
        />
        <div class="flex ml-6 pt-2 pb-5 gap-1">
          <input class="" type="checkbox" />
          <p class="text-body text-[12px]">Recuerdame</p>
        </div>
      </div>
      <div class="w-fit mx-auto sm:-mb-5 mb-[-9%]">
        <router-link
          to="/company"
          class="text-lightGrey font-extralight bg-darkGrey py-2 px-3 sm:px-6 rounded-full text-2xl"
        >
          lniciar sesion
        </router-link>
      </div>
    </div>
  </div>
</template>
