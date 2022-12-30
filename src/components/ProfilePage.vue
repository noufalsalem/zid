<template>
<div>
    <h1>{{ prof }}</h1>
</div>

<!-- Classes in the following 
    are from bootstrap. 
    See main.ts for import-->

<section class="vh-100">
  <div class="container py-5 h-100">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col col-lg-6 mb-2 mb-lg-0">
        <div class="card mb-3" style="border-radius: .5rem;">
          <div class="row g-0">
            <div class="col-md-4 gradient-custom text-center text-white"
              style="border-top-left-radius: .5rem; border-bottom-left-radius: .5rem;">
              <img src="../assets/zid-logo.png"
                alt="Avatar" class="img-fluid my-5" style="width: 80px;" />
              <h4>Name AlName</h4>
              <p>Occupation</p>
              <p>Born Nov. 25, 1997 </p>
                <a href="#!"><i class="fa fa-facebook fa-lg"></i></a>
                <a href="#!"><i class="fa fa-twitter fa-lg"></i></a>
                <a href="#!"><i class="fa fa-instagram fa-lg"></i></a>
                
            </div>
            <div class="col-md-8">
              <div class="card-body p-4">
                <h5>Information</h5>
                <hr class="mt-0 mb-4">
                <div class="row pt-1">
                  <div class="col-6 mb-3">
                    <h5>Email</h5>
                    <p class="text-muted">info@example.com</p>
                  </div>
                  <div class="col-6 mb-3">
                    <h5>Gender</h5>
                    <p class="text-muted">Female</p>
                  </div>
                </div>
                <h5>Projects</h5>
                <hr class="mt-0 mb-4">
                <div class="row pt-1">
                  <div class="col-6 mb-3">
                    <h5>Recent</h5>
                    <p class="text-muted">Lorem ipsum</p>
                  </div>
                  <div class="col-6 mb-3">
                    <h5>Most Viewed</h5>
                    <p class="text-muted">Dolor sit amet</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    prof: String
  }
})
export default class ProfilePage extends Vue {
  prof!: string
}
</script>

<style scoped>
@import url("//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css");

h1 {
    margin: 40px 0 0;
}

.fa {
    color: #FFCF4B;
    outline: black;
}

p {
    font-size:medium;
}

.gradient-custom {

background: #86589E;

background: -webkit-linear-gradient(to right bottom, rgba(246, 211, 101, 1), rgba(253, 160, 133, 1));

background: linear-gradient(to right bottom, rgba(209, 181, 223, 1), rgba(134, 88, 158, 1))
}

a {
    margin: 10px;
}

section {
    margin: -200px;
}


</style>
