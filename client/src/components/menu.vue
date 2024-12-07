<script setup>
// fatch запрос читающий json
    import ProductItem from './product-item.vue';

    import { ref } from 'vue';

    const isActive = ref(1);

    const isActivationUpdate = (productId) => {
        isActive.value = productId;
    };
</script>

<template>
    <article id="menu" class="menu">
        <h1 class="heading">Menu</h1>
        <section class="category" id="category">
            <article class="category-box" :class="{active: isActive === 1}" @click.prevent="isActivationUpdate(1)">
                <i class="fas fa-hot-tub"></i>
                <span class="h5-font">hotter</span>
            </article>
            <article class="category-box" :class="{active: isActive === 2}" @click.prevent="isActivationUpdate(2)">
                <i class="fas fa-utensils"></i>
                <span class="h5-font">starters</span>
            </article>
            <article class="category-box" :class="{active: isActive === 3}" @click.prevent="isActivationUpdate(3)">
                <i class="fas fa-birthday-cake"></i>
                <span class="h5-font">desserts</span>
            </article>
            <article class="category-box" :class="{active: isActive === 4}" @click.prevent="isActivationUpdate(4)">
                <i class="fas fa-wine-bottle"></i>
                <span class="h5-font">drinks</span>
            </article>
        </section>
        <h1 class="heading">Products</h1>
        <section class="product" id="menu">
            <article class="product-box" v-if="isActive === 1">
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healthy" text="$15.99" spanTxt="20.99" btn="add to cart" /> 
                <ProductItem imgPath="../../public/eat-2.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-3.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-4.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-5.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-6.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
            </article>
            <article class="product-box" v-if="isActive === 2">
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-2.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-3.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-4.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-5.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-6.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
            </article>
            <article class="product-box" v-if="isActive === 3">
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healthy" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-2.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-3.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-4.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-5.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-6.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/eat-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
            </article>
            <article class="product-box" v-if="isActive === 4">
                <ProductItem imgPath="../../public/menu.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-2.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-3.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-4.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-1.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
                <ProductItem imgPath="../../public/drink-2.jpg" title="tasty and healty" text="$15.99" spanTxt="20.99" btn="add to cart">
                </ProductItem>
            </article>
        </section>
    </article>
</template>

<style scoped lang="scss">
    @import '../assets/styles/menu.scss';
    @import '../assets/styles/fonts.scss';
</style>