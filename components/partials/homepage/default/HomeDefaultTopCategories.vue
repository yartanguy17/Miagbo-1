<template lang="html">
    <div class="ps-top-categories" v-if="!$fetchState.pending">
        <div class="ps-container">
            <h3>{{ $t('autopart.topCategories') }}</h3>
            <div class="row">
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>                        
                        <img
                            :src="baseUrl + categories[0].img"
                            alt="martfury"
                        />
                        <p>{{categories[0].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[1].img"
                            alt="martfury"
                        />
                        <p>{{categories[1].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[2].img"
                            alt="martfury"
                        />
                        <p>{{categories[2].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[3].img"
                            alt="martfury"
                        />
                        <p>{{categories[3].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[4].img"
                            alt="martfury"
                        />
                        <p>{{categories[4].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[5].img"
                            alt="martfury"
                        />
                        <p>{{categories[5].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[6].img"
                            alt="martfury"
                        />
                        <p>{{categories[6].nom}}</p>
                    </div>
                </div>
                <div class="col-xl-2 col-lg-3 col-md-4 col-sm-4 col-6 ">
                    <div class="ps-block--category">
                        <nuxt-link to="/shop">
                            <a class="ps-block__overlay"></a>
                        </nuxt-link>
                        <img
                            :src="baseUrl + categories[7].img"
                            alt="martfury"
                        />
                        <p>{{categories[7].nom}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeDefaultTopCategories',
    data(){
        return{
            baseUrl: 'http://51.89.97.33:5500',
            categories: [],
        }
    },
    async fetch(){
        this.categories = await fetch('http://51.89.97.33:5500/api/categories')
            .then(res => res.json());
    }
};

</script>

<style lang="scss" scoped></style>
