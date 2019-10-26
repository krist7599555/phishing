<template>
<div id='head-label'>
  <slot/>
  <h1 style='margin-bottom: 10px'>
    <span>กรอกข้อมูลเพื่อรับ E-book </span>
    <div class="tag is-info">ฟรี!!</div>
  </h1>
  <img class='book' src="../assets/book.jpg" alt="book">
  <h1 class='has-text-danger is-size-4'>
    <b>"รู้เท่าทันมิจฉาชีพออนไลน์"</b>
  </h1>
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
#head-label {
  padding: 2rem 3rem;
  padding-top: 5rem;
  background-color: #eeeeee;
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
.book {
  margin: 2rem;
  max-height: 200px;
  box-shadow: 9px 7px 8px 1px #858282b3;
}
</style>
