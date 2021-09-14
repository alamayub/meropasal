<template>
  <div style="background-color: rgb(0 0 0 / 5%); min-height: 90vh;">
    <v-container>
      <div class="display-1 mb-2">My Cart</div>  
      <div class="cart">
        <div class="cart__items d-flex flex-column" style="grid-gap: 12px;">
          <div class="cart__item white d-flex" v-for="a in 5" :key="a">
            <div class="cart__item__img">
              <img src="https://assets.myntassets.com/dpr_1.5,q_60,w_400,c_limit,fl_progressive/assets/images/10856160/2019/11/5/f0172470-408a-4b8b-a1e5-045bd98a5f8b1572938035104-SASSAFRAS-Women-Dresses-9581572938032856-1.jpg" alt="Dress Name">
            </div> 
            <div class="cart__item__content d-flex flex-column justify-space-between pa-3">
              <div>
                <div class="title">Dress Name</div>  
                <div style="line-height: 1; font-size: 13px; color: grey;">Dress, L</div>
              </div>
              <div class="d-flex">
                <v-btn icon tile small outlined color="primary">
                  <v-icon small>mdi-minus</v-icon>
                </v-btn>
                <div style="height: 28px; width: 28px; font-size: 12px; border-bottom: 1px solid blue; border-top: 1px solid blue;" class="d-flex align-center justify-center">5</div>
                <v-btn icon tile small outlined color="primary">
                  <v-icon small>mdi-plus</v-icon>
                </v-btn>  
              </div>
              <div style="line-height: 1;">
                <div class="cart__item__content__rating d-flex align-end">
                  <v-rating color="amber" readonly size="16" half-increments dense :value="3.5" />  
                  &nbsp;<span>(32454)</span>
                </div>
                <div class="cart__item__content__price mt-1">
                  <span>Rs.2500</span>&nbsp;<span><del><i>(Rs.3000)</i></del></span>&nbsp;<span>(20% off)</span>
                </div>  
              </div>
            </div> 
          </div>
        </div>  
        <div class="cart__total white d-flex flex-column justify-space-between">
          <div>
            <div class="title d-flex align-center justify-center" style="height: 80px;">Cart Total</div>  
            <v-divider />
            <div class="d-flex justify-space-between px-3 py-2">
              <span>Sub Total</span><span>Rs.5020</span>  
            </div>
            <v-divider />
            <div class="d-flex justify-space-between px-3 py-2">
              <span>Discount</span><span>Rs.1020</span>  
            </div>
            <v-divider />
            <div class="d-flex justify-space-between px-3 py-2">
              <span>Grand Total</span><span>Rs.4000</span>  
            </div>  
          </div>
          <div class="d-flex px-3 pb-8">
            <v-btn rounded block color="primary" style="font-weight: 300 !important; text-transform: capitalize !important;">checkout</v-btn>  
          </div>
        </div>
      </div>
    </v-container>
  </div>  
</template>

<style scoped>
.cart {
  display: grid;
  grid-template-columns: 75% 25%;  
  grid-gap: 20px;
}
.cart__item {
  overflow: hidden;
  position: relative;  
  transition: ease-in-out 250ms;
  cursor: pointer;
}
.cart__item:hover {
  border-radius: 4px;
  box-shadow: 0 1px 10px 0 rgb(0 0 0 / 15%);
  transform: translateY(-6px);  
}
.cart__item__img img { max-height: 150px; }
.cart__item__content__price { line-height: 1; }
.cart__item__content__price span:first-child { color: #000; }
.cart__item__content__price span:nth-child(2), .cart__item__content__rating span { font-size: 12px; color: grey; line-height: 1; }
.cart__item__content__price span:last-child { font-size: 12px; color: green; }

.cart__total {
  border-radius: 6px;
  overflow: hidden;
  max-height: 320px;  
}
</style>