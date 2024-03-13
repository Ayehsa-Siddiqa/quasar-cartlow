<template>
<q-page>
    <div :class="$q.screen.gt.lg ? 'container q-px-sm' : 'q-px-lg' ">
        <div class="row justify-center q-py-md">
           <q-img src="public/images/imgBAr.webp" class="rounded-borders" width="99%"/> 
        </div>
    </div>
    <!-- home carousel section start -->
    <div :class="$q.screen.gt.lg ? 'container q-px-sm' : 'q-px-lg' ">
        <homeCarousel :homeCarousel="slidesObj" />
    </div>

    <!-- product sec 1 start -->
    <div :class="$q.screen.gt.lg ? 'container q-px-sm' : 'q-px-lg' ">
        <div class="row q-col-gutter-lg q-py-lg">
            <productSec1 :productsArr="productSec1Arr" />
        </div>
    </div>
    <!-- product sec 1 end -->

    <!-- product section 2 start Ramdan's low cart -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <commenProductComponent :product2Arr="ramdanCarrArr" :productObj="productObj" />
    </div>
    <!-- product section 2 end Ramdan's low cart -->

    <!-- smartPhone Heaven section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <smartPhoneHeavn :smartObj="smartHeavenObj" />
    </div>
    <!-- smartPhone Heaven section end-->

    <!-- top rated i phone section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden q-pt-lg">
        <commenProductComponent :product2Arr="topRatedIphoneArr" :productObj="topIphoneObj" />
    </div>
    <!-- top rated i phone section -->

    <!-- top rated Androids section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden q-pt-lg">
        <commenProductComponent :product2Arr="topRatedAndroidsArr" :productObj="topAndriodsObj" />
    </div>
    <!-- top rated Androids section -->

    <!-- popular Apple watch Picks section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden q-pt-lg">
        <commenProductComponent :product2Arr="popularWatchArr" :productObj="popularWatchObj" />
    </div>
    <!-- popular Apple watch Picks section-->

    <!-- Popular Choices section start -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <commenComponent2 :dataObj="popularChoices" />
    </div>  
    <!-- Popular Choices section end -->

    <!-- Best Selling Laptops section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden q-pt-lg">
        <commenProductComponent :product2Arr="bestSellingLaptopsArr" :productObj="bestSellingLaptopsObj" />
    </div>
    <!-- Best Selling Laptops section end-->

    <!-- loved Fragrances section start -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <commonComponent3 :commonObj3="lovedFragrance" />
    </div> 
     <!-- loved Fragrances section end -->

     <!-- shope watches section start -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <commonComponent3 :commonObj3="shopWatches" />
    </div> 
    <!-- shope watches section end -->

    <!-- Our products condition section start --> 
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' " class="overflow-hidden">
        <productCondition :productCondition="productCondition"/>
    </div> 
    <!-- Our products condition section start -->


    <!-- Top Brands on Appliances sec -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' ">
        <commonComponent3 :commonObj3="topAppliances"/>
    </div> 
     <!-- Top Brands on  Appliances sec end -->

    <!-- wellcome to cart section start -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' ">
        <wellcomeCartlow/>
    </div>  
    <!-- wellcome to cart section end -->

    <!-- happy Customers section -->
    <div :class="$q.screen.gt.lg? 'container q-px-sm' : 'q-px-lg' ">
        <happyCustomer/>
    </div>
    <!-- happy Customers section end-->



</q-page>
</template>

<script>
import {
    defineComponent
} from 'vue'
import productSec1 from 'components/productSec1.vue'
import homeCarousel from 'src/components/homeCarousel.vue';
import commenProductComponent from 'src/components/commenProductComponent.vue';
import smartPhoneHeavn from 'src/components/smartPhoneHeavn.vue';
import commenComponent2 from 'src/components/commenComponent2.vue';
import commonComponent3 from 'src/components/commonComponent3.vue';
import productCondition from 'src/components/productCondition.vue';
import wellcomeCartlow from 'src/components/wellcomeCartlow.vue';
import happyCustomer from 'src/components/happyCustomer.vue';

export default defineComponent({
    name: 'IndexPage',
    components: {
        homeCarousel,
        productSec1,
        commenProductComponent,
        smartPhoneHeavn,
        commenComponent2,
        commonComponent3,
        productCondition,
        wellcomeCartlow,
        happyCustomer,

    },
    data() {
        return {
            // home carousel sec
            slidesObj: [
                "/images/homeCarousel/img1.webp",
                "/images/homeCarousel/img2.webp",
                "/images/homeCarousel/img3.webp",
                "/images/homeCarousel/img4.webp",
                "/images/homeCarousel/img5.webp",
                "/images/homeCarousel/img6.webp",
            ],
            // product section1 Arr
            productSec1Arr: [{
                    pic: 'images/productSec1/product1.webp'
                },
                {
                    pic: 'images/productSec1/product2.webp'
                },
                {
                    pic: 'images/productSec1/product3.webp'
                },
                {
                    pic: 'images/productSec1/product4.webp'
                }
            ],
            // ramdans' low cart section
            productObj: {
                title: " Ramadan's Low Cart"
            },
            ramdanCarrArr: [{
                    productImg: "images/ramdanCartLowProdSec2/AcerR11.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple and this is a new offer by Ramzan",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/iphone7.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/iphone12.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/iphone13.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/AcerR11.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/AcerR11.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/AcerR11.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/ramdanCartLowProdSec2/AcerR11.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
            ],
            // smartPhoneHeaven section
            smartHeavenObj: {
                title: "Smartphone Heaven",
                img1: "images/smartPhoneHeaven/img1.webp",
                img2: "images/smartPhoneHeaven/img2.webp",
                img3: "images/smartPhoneHeaven/img3.webp",
                img4: "images/smartPhoneHeaven/img4.webp",
                img5: "images/smartPhoneHeaven/img5.webp",
            },
            // top Rated iphone section 
            topIphoneObj: {
                title: "Top Rated iphones"
            },
            topRatedIphoneArr: [{
                    productImg: "images/topRatedIphone/img1.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img2.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img3.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img4.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img5.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img4.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img2.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/topRatedIphone/img3.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
            ],
            // top Rated android section 
            topAndriodsObj: {
                title: "Top Rated Andriods"
            },
            topRatedAndroidsArr: [{
                    productImg: "public/images/topRatedAndroids/img1.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img2.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img3.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img4.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img5.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img6.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img7.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "public/images/topRatedAndroids/img1.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
            ],
            //popular Apple watche section 
            popularWatchObj: {
                title: "Popular Apple watche Picks"
            },
            popularWatchArr: [{
                    productImg: "images/popularAppleWatches/img1.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img2.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img3.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img4.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img5.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img6.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img7.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img8.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/popularAppleWatches/img9.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
            ],
            // Popular Choices section
            popularChoices: {
                title: "Popular Choices",
                img1: "images/popularChoices/img1.webp",
                img2: "images/popularChoices/img2.webp",
                img3: "images/popularChoices/img3.webp",
                img4: "images/popularChoices/img4.webp",
            },    
         // best selling laptops section 
         bestSellingLaptopsObj: {
                title: "Best Selling Laptops"
            },
            bestSellingLaptopsArr: [{
                    productImg: "images/bestSellingLaptops/img1.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img2.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img3.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img4.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img5.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img6.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img7.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img8.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img9.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
                {
                    productImg: "images/bestSellingLaptops/img10.webp",
                    nameOfProduct: "Apple iPhone 14 Pro Max 256 GB - Deep Purple",
                    condition: " Pre-Loved | Top",
                    currency: "AED 3780.00",
                    mainPrice: " AED 4,735.00",
                    discount: "20%  less vs. new",
                    delivery: "only  4 left - order now."

                },
            ],
            //  loved Fragrances sec
            lovedFragrance :{
                title:"loved Fragrances",
                img1:"images/lovedFaragrances/img1.webp",
                img2:"images/lovedFaragrances/img2.webp",
                img3:"images/lovedFaragrances/img3.webp", 
            },
            // shope watches section
            shopWatches:{
                title:"Shope Watches",
                img1:"images/shopWatches/img1.webp",
                img2:"images/shopWatches/img2.webp",
                img3:"images/shopWatches/img3.webp", 
            },
            // Our products condition section
            productCondition:[
             {
               title:"Pre-Loved | Top",
               upTo:"Up to",
               percent:"70% ",
               percentLess:" less vs. new",
               desc1:"An original product",
               desc2:"Lightly used",
               desc3:"100% functionality test by Experts",
               highlight:"* Item will be delivered in Cartlow packaging with all compatible accessories" 
             },
             {
               title:"Pre-Loved | Top",
               upTo:"Up to",
               percent:"70% ",
               percentLess:" less vs. new",
               desc1:"An original product",
               desc2:"Lightly used",
               desc3:"100% functionality test by Experts",
               highlight:"* Item will be delivered in Cartlow packaging with all compatible accessories" 
             },
             {
               title:"Pre-Loved | Top",
               upTo:"Up to",
               percent:"70% ",
               percentLess:" less vs. new",
               desc1:"An original product",
               desc2:"Lightly used",
               desc3:"100% functionality test by Experts",
               highlight:"* Item will be delivered in Cartlow packaging with all compatible accessories" 
             },
             {
               title:"Pre-Loved | Top",
               upTo:"Up to",
               percent:"70% ",
               percentLess:" less vs. new",
               desc1:"An original product",
               desc2:"Lightly used",
               desc3:"100% functionality test by Experts",
               highlight:"* Item will be delivered" 
             },

            ],
             //  Top Brands on Appliances sec
             topAppliances :{
                title:"Top Brands on Appliances",
                img1:"images/topAppliances/img1.webp",
                img2:"images/topAppliances/img2.webp",
                img3:"images/topAppliances/img3.webp", 
            },

        }
    }
})
</script>
