<template>

  <div class="sw-register-form" >
    <div class="sw-form-heading">
      <mr-logo style="height:42px;width:42px;margin:5px; display:inline-block"></mr-logo>
      <div>User Registration</div>
    </div>
    <div style="padding:10px">
      <user-details :rec="{userId:'NEW', role:'CUSTOMER'}" :isCustomer="true" > </user-details>
    </div>
  </div>
</template>

<script>
import Rest from '@/rest/Rest';
import router from '@/router';
import MrLogo from '@/components/logo/Logo';
import UserDetails from '@/views/UserDetails'

export default {

  components: {
    MrLogo,
    UserDetails
  }

}
</script>
<style lang="scss" scoped>
@import "~@/assets/styles/_vars.scss";

$sw-form-width:600px;

.sw-register-form{
  top : 24px;
  left: calc(50% - #{$sw-form-width/2});
  position: absolute;
  border: 1px solid #333;
  border-top-width: 3px;
  width:$sw-form-width;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  .sw-form-heading{
    //background-color: #333;
    height:60px;
    color:#333;
    display:flex;
    justify-content: start;
    align-items: center;
    font-size: 24px;
  }
}



</style>

