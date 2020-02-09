<template>
<scroll-view class="container" :content-container-style="{contentContainer: {
        paddingVertical: 20
    }}">
    <view class="header">
      <text class="txt-header">{{txtHeader}}</text>
    </view>
    <view class="divider"></view>
    <view class="body">
      <view class="card-product" v-for="product in products" :key="product.txtApiName">
        <view class="card-product-name">
          <text class="txt-card-product">{{txtName}}</text>
          <text class="txt-card-product-api">{{product.txtApiName}}</text>
        </view>
          <text class="txt-card-product">{{txtPrice}}</text>
          <text class="txt-card-product-api">{{product.txtApiPrice}}</text>
          <text class="txt-card-product">{{txtAmount}}</text>
          <text class="txt-card-product-api">{{product.txtApiAmount}}</text>

          <view class="card-product-button">
            <button class="card-product-button-edit" title="Editar"/>
            <button class="card-product-button-delete" color="#FF4646" title="Deletar"/>
          </view>
      </view>
    </view>
    <view class="footer">
      <button class="footer-button" title="Cadastrar"/>
    </view>
</scroll-view>
</template>

<script>
export default {
data() {
  return {
    txtHeader:"Produtos",
    txtName: "Nome:",
    txtPrice: "Preço:",
    txtAmount: "Quantidade:",
    products:[
      {
        txtApiName: "Produto 1",
        txtApiPrice: 20.00,
        txtApiAmount: 5,
      },
      {
        txtApiName: "Produto 2",
        txtApiPrice: 50.00,
        txtApiAmount: 10,
      },
      {
        txtApiName: "Produto 3",
        txtApiPrice: 15.44,
        txtApiAmount: 50,
      },
      {
        txtApiName: "Produto 4",
        txtApiPrice: 10,
        txtApiAmount: 9,
      },

    ]
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
  margin: 20px;
  width: 100%;
  border-color: #707070;
}
.body{
  margin-left: 10px;
  margin-right: 10px;
}
.card-product{
  width: 100%;
  height: 200px;
  background-color: #fff;
  border-radius: 10px;
  margin-bottom: 11px;
}
.card-product-name{
  flex: 0;
}
.txt-card-product{
  font-size: 20px;
  font-weight: bold;
  font-family: sans-serif;
}
.txt-card-product-api{
  font-size: 20px;
}
.card-product-button{
  margin-left: 5px;
  margin-right: 5px;
}
.card-product-button-edit{
  max-width: 150px;
}
.footer{
  margin-bottom: 5px;
  margin-right: 10px;
  margin-left: 10px;
  margin-top: 20px;
}
</style>
