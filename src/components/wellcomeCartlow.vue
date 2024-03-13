<template>
<div class="q-px-lg">
    <div class="bg-white rounded-borders">
        <div class="row">
            <div class="col-12 col-md-8">
                <div class="content q-py-lg q-px-xl">
                    <div class="text-h5">
                        Welcome to Cartlow, where shopping smart and saving big go hand in hand!
                    </div>
                    <div class="text-weight-regular fs-15 q-py-lg">
                        We're the number one re-commerce platform in the GCC and our mission is all about you. Shop with confidence and score big discounts, up to 80%, on top-quality, gently-used products. And don't worry, every purchase is backed by a 12-month warranty for your peace of mind. Help us give pre-loved products a second chance, save money, and make a positive impact on the environment – all while shopping at Cartlow!
                    </div>
                    <div class="row">
                        <div class="col-6 col-md-3" v-for="data in dataArr" :key="data">
                            <q-img :src="data.src" width="80px" height="80px" class="block q-mr-auto" />
                            <div class="text-subtitle2 q-pl-md">
                                {{data.label}}
                            </div>
                            <div class="text-h5 text-weight-bold q-pl-lg">
                                {{data.howMany}}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-12 col-md-4">
                <div class="background-img">

                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    // name: 'ComponentName',
    data() {
        return {
            dataArr: [{
                    src: "images/wellcomeSec/img1.png",
                    label: "Years",
                    howMany: "4+",
                },
                {
                    src: "images/wellcomeSec/img2.png",
                    label: "Countries",
                    howMany: "4",
                },
                {
                    src: "images/wellcomeSec/img3.png",
                    label: "Employees",
                    howMany: "200 +",
                },
                {
                    src: "images/wellcomeSec/img4.png",
                    label: "Happy Customers",
                    howMany: "2M+",
                }
            ]
        }
    }
}
</script>

<style scoped>
.background-img {
    background-image: url('images/wellcomeSec/welcomeBgImg.png');
    width: 100%;
    height: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 5px; 
}
</style>
