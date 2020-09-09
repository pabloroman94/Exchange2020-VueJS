<template>
  <header class="shadow w-screen">
    <nav>
      <nav class="flex items-center justify-between flex-wrap bg-green-400 p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <PrIcon class="mr-2" />

          <router-link 
          :to="{name: 'home'}" class="font-semibold mx-2 text-xl tracking-tight"
            >PabloRomanExchange  
          </router-link>
            <router-link 
            v-for="l in links"
            :key="l.title"
            :to="l.to"
            class="block mx-2 mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4" >
            {{l.title}}</router-link>


        </div>
        <!-- <div class="hidden sm:block w-full blok flex-grow lg:flex lg:items-center lg:wauto" >
          <div class="text-sm lg:flex-grow">
          </div>
        </div> -->
      </nav>
    </nav>
  </header>
</template>

<script>
import PrIcon from "@/components/PrIcon";

export default {
  neme: "PrHeader",
  components: {
    PrIcon
  },
  props:{
    links: Array,
    default:()=>{}
  }
};
</script>
