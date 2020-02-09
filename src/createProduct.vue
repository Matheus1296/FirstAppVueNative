<template>
  <view class="container">
    <view class="header">
      <text class="txt-header">{{txtHeader}}</text>
    </view>
    <view class="divider"></view>
    <view class="body">
      <text class="txt-body">{{txtName}}</text>
      <text class="txt-body">{{txtPrice}}</text>
      <text class="txt-body">{{txtAmount}}</text>
    </view>
    <view class="footer">
      <button class="footer-button" title="Cadastrar"/>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      txtHeader: "Cadastro de Produtos",
      txtName: "Nome:",
      txtPrice: "Preço:",
      txtAmount: "Quantidade:"
    }
  },
}
</script>

<style scoped>
.container {
  background-color: #DFDFDF;
  width: 100%;
  height: 100%;
  flex: 1;
}
.header{
  margin-top: 30px;
  margin-left: auto;
  margin-right: auto;
}
.txt-header{
  color: black;
  font-size: 30px;
  font-family: sans-serif;
  font-weight: bold;
}
.divider{
  margin-top: 10px;
  margin-bottom: 10px;
  width: 100%;
  height: 1px;
  background-color: #707070;
}
.body{
  margin-left: 10px;
}
.txt-body{
  font-size: 20px;
  color: black;
  margin: 3px;
}

.footer{
  margin-left: 10px;
  margin-right: 10px;
}

</style>