<template>
  <view class="container">
    <view class="header">
      <text class="txt-header">{{txtHeader}}</text>
    </view>
    <view class="divider"></view>
    <view class="body">
      <text class="txt-body">{{txtName}}</text>
      <text-input
        :style="{height: 50, borderRadius:10, backgroundColor:'#fff'}"
        v-model="inputName"
      />
      <text class="txt-body">{{txtPrice}}</text>
      <text-input
        :style="{height: 50, borderRadius:10, backgroundColor:'#fff'}"
        v-model="inputPrice"
      />
      <text class="txt-body">{{txtAmount}}</text>
      <text-input
        :style="{height: 50, borderRadius:10, backgroundColor:'#fff'}"
        v-model="inputAmount"
      />
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
      txtAmount: "Quantidade:",
      inputName: "",
      inputPrice: 0,
      inputAmount: 0,
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
  margin-right: 10px;
}
.txt-body{
  font-size: 20px;
  color: black;
  margin: 3px;
}

.footer{
  margin-top: auto;
  margin-bottom: 10px;
  margin-left: 10px;
  margin-right: 10px;
}

</style>