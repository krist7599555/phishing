<template>
<div id='login-form'>
  <button class="button is-info" style='background-color: #4968AD'>
    <img class='fb-logo' src="../assets/facebook.svg" alt="facebook logo"/>
    <span>
      Sign Up With Facebook
    </span>
  </button>
  <br>
  <br>
  <div class="help">or with email</div>
  <br>
  <form @submit.prevent>
    <template v-for='f in fields'>
      <div class="field" :key='f'>
        <div class="control">
          <input type="text" class="input" :placeholder="f">
        </div>
      </div>
    </template>
    <br>
    <button class="button is-info" type='submit' style='background-color: #e17424'>
      <img class='ebook-logo' src="../assets/ebook.png" alt="ebook logo" >
      <b>Download E-Book</b>
    </button>
  </form>
</div>
</template>

<script>
const fields = [
  "Full Name | ชื่อ - นามสกุล",
  "Identification Number | เลขประจำตัวประชาชน",
  "Phone Number | หมายเลขโทรศัพท์",
  "Email | อีเมลล์",
  "Birthdate | วันเกิด",
  "Gender | เพศ",
]
export default {
  name: 'Form',
  data() {
    return {
      fields
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#login-form {
  max-width: 320px;
}
.fb-logo,
.ebook-logo {
  width: 25px;
  filter: invert(148%) sepia(79%) saturate(2476%) hue-rotate(186deg) brightness(118%) contrast(119%);
}
.fb-logo {
  margin-right: 15px;
  filter: invert(148%) sepia(79%) saturate(2476%) hue-rotate(186deg) brightness(118%) contrast(119%);
}
.ebook-logo {
  margin-left: -5px;
  margin-right: 10px;
  filter:  invert(174%) sepia(84%) saturate(2476%) hue-rotate(264deg) brightness(249%) contrast(141%)
}
</style>
