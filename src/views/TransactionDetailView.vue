<script setup>
import { mdiBallotOutline } from '@mdi/js'
import SectionMain from '@/components/SectionMain.vue'
import CardBox from '@/components/CardBox.vue'
import LayoutAuthenticated from '@/layouts/LayoutAuthenticated.vue'
import SectionTitleLineWithButton from '@/components/SectionTitleLineWithButton.vue'

</script>

<template>
  <LayoutAuthenticated>
    <SectionMain>
      <SectionTitleLineWithButton :icon="mdiBallotOutline" title="Detail Transaksi" main />
      <CardBox class="mb-6" has-table>
        <table class="min-w-full">
          <thead>
            <tr>
              <th>Id Product</th>
              <th>Jumlah Produk</th>
              <th>Subtotal</th>
              <th>Kembalian</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(product, index) in products" :key="index">
              <td>{{ product.id_product }}</td>
              <td>{{ product.jumlah_produk }}</td>
              <td>{{ product.subtotal }}</td>
              <td>{{ product.kembalian }}</td>
            </tr>
          </tbody>
        </table>
      </CardBox>
    </SectionMain>
  </LayoutAuthenticated>
</template>
