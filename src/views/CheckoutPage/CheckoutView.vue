<script setup lang="ts">
import Details from '@/views/CheckoutPage/Details.vue';
import Options from '@/views/CheckoutPage/Options.vue';
import PriceSection from '@/views/CheckoutPage/PriceSection.vue';
import TableSection from '@/views/CheckoutPage/TableSection.vue';
import Table2 from '@/views/CheckoutPage/Table2.vue'
import StockCard from '@/views/CheckoutPage/StockCard.vue';

</script>

<template>
  <div class="bg-white dark:bg-extradarkGrey">
    <Options/>
    <div class="flex flex-wrap justify-between ">
    <div >
      <Details/>
    <TableSection/>
    <div class="flex justify-between">
      <Table2/>
      <StockCard/>
    </div>
    </div>
    <div class="sm:w-full lg:w-auto">
      <PriceSection/>
    </div>
  </div>
  </div>


</template>

