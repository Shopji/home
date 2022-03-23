<template>
  <div class="max-width-1200 margin-auto">
      <div class="w-layout-grid grid-4">
        <div>
          <div class="footer-logo"></div>
          <p class="footer-text">{{$t('footer.title1')}}</p>
          <a data-position="footer" target="_blank" href="https://shopji.co/#/pages/modules/mall/partner/applyPartner" class="primary-button startselling w-button">{{$t('startselling')}}</a>
        </div>
        <div id="w-node-_56e1e3b0-5d79-51bb-79e9-13175659d6ab-088bf3ae"></div>
        <div>
          <h5 class="footer-title">{{$t('footer.title2.title')}}</h5>
          <nuxt-link :to="localePath('/howto/seller')" target="_blank" class="footer-link">{{$t('footer.title2.details.i1')}}</nuxt-link>
          <nuxt-link  :to="localePath('/howto/supplier')"  target="_blank" class="footer-link">{{$t('footer.title2.details.i2')}}</nuxt-link>
          <nuxt-link :to="localePath('/howto/shipping')" target="_blank" class="footer-link">{{$t('footer.title2.details.i3')}}</nuxt-link>
          <a :href="'https://shopji.co/policies/'+$i18n.locale" target="_blank" class="footer-link">{{$t('footer.title2.details.i4')}}</a>
        </div>
        <div>
          <h5 class="footer-title">{{$t('footer.title3')}}</h5>
          <a href="mailto:sell@shopji.co" class="footer-link">sell@shopji.co</a>
          <div class="flex-wrap">
            <a href="https://www.instagram.com/sellonshopji/" target="_blank" class="footer-social-link w-inline-block"><img src="~/assets/images/instagram.svg" loading="lazy" alt="Instagram"></a>
            <a href="https://www.facebook.com/sellonshopji" target="_blank" class="footer-social-link w-inline-block"><img src="~/assets/images/facebook.svg" loading="lazy" alt="Facebook"></a>
          </div>
        </div>
      </div>
      <div class="space-30"></div>
      <div class="line"></div>
      <div class="space-30"></div>
      <p class="footer-copyright">© {{new Date().getFullYear()}} Shopji Technologies. All Rights Reserved.</p>
      <div class="space-10"></div>
    </div>
</template>
