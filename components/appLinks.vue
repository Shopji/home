<template>
    <ul class="nav-list">
        <li class="nav-item nav-link-2 w-nav-link  w--nav-link-open"><nuxt-link :to="localePath('/')">{{$t('applinks.shopjiintro')}}</nuxt-link></li>
        <li class="nav-item nav-link-2 w-nav-link  w--nav-link-open"><nuxt-link :to="localePath('/howto/seller')">{{$t('applinks.sellerguide')}}</nuxt-link></li>
        <li class="nav-item nav-link-2 w-nav-link  w--nav-link-open"><nuxt-link :to="localePath('/howto/supplier')">{{$t('applinks.supplierguide')}}</nuxt-link></li>
        <li class="nav-item nav-link-2 w-nav-link  w--nav-link-open"><nuxt-link :to="localePath('/howto/shipping')">{{$t('applinks.shipping')}}</nuxt-link></li>
    </ul>
</template>

<style lang='scss' scoped>
    .nav-list {
        list-style: none;
        padding: 0;
        margin: 0;
    }
    .nav-item {
        margin: 0 10px;
    }
    .nav-item a {
        text-decoration: none;
        color: #111;
    }
     .nav-item a:hover,
    .nav-item a:active{
      color:$color_primary

    }

    .nav-item {
        .nuxt-link-active{
          color: $color_primary;
        }

    }

    @media (max-width: 767px) {
        .nav-list {
            display: block;
        }
        .nav-item{
            margin-top: 16px;
            margin-bottom: 16px;
        }
    }
    @media (min-width: 768px) {
        .nav-list {
            display: flex;
        }
    }
</style>
