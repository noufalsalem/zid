<template>
  <div class="profile">
 <ProfilePage prof="Profile Card"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import ProfilePage from '@/components/ProfilePage.vue'; 

@Options({
  components: {
    ProfilePage,
  },
})
export default class ProfileView extends Vue {}
</script>
