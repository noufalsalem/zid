<template>
    <div class="credit">
 <CreditPage crdMsg="Payment Details"/>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CreditPage from '@/components/CreditPage.vue'; 

@Options({
  components: {
    CreditPage,
  },
})
export default class CreditView extends Vue {}
</script>
