<script setup>
import { defineProps } from 'vue';
import { RouterLink} from 'vue-router'

const props = defineProps({
  title: String,
  link: String,
  text: String,
});
</script>

<template>
<section class="form_element vh-100">
  <div class="container h-100">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col col-xl-10">
        <div>
          <div class="row">
            <div class="col-md-6 col-lg-5 d-flex align-items-center justify-content-center">
              <div class="img_container">
                <img src="@/assets/todo.png"
                alt="guy with papers"  />
            </div>
              </div>
            <div class="col-md-6 col-lg-7 text-center">
              <div>

                <form class="text-white">
                  <div class="d-flex align-items-center">
                    <div class="logo">
                      <img src="@/assets/logo.svg"
                      alt="logo"  />
                    </div>
                    <h1>TO DO</h1>
                  </div>

                  <h5>Sign into your account</h5>

                  <div class="form-outline">
                    <input type="email" id="email" class="form-control form-control-lg" />
                    <label class="form-label" for="email">Email address</label>
                  </div>

                  <div class="form-outline">
                    <input type="password" id="password" class="form-control form-control-lg" />
                    <label class="form-label" for="password">Password</label>
                  </div>

                  <div>
                    <button class="btn btn-light btn-lg btn-block" type="button">Login</button>
                  </div>

                  <p>{{ text }}? <RouterLink :to="`/${link}`">{{ link }}</RouterLink></p>

                  <a href="#">Forgot password?</a>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

</template>

<style scoped lang="scss">
.form_element{
  .logo{
    background-color:white;
    width:50px;
    padding:10px;
    border-radius:50%;
    margin-right:20px;
  }
      img{
        height:100%;
        width:100%;
        object-fit:cover;
      }
    form{
      padding:50px;
      border-radius:20px;
      background-color:black;
    }
}
</style>