<template>
    <header>
        <div class="brand-name">
           <nuxt-link class="topMenu home" to="/" style="float:left;"></nuxt-link>

        </div>

        <div class="actions-section">
                <a data-position="header" target="_blank"  href="https://shopji.co/#/pages/modules/mall/partner/applyPartner" class="primary-button startselling w-button">{{$t('startselling')}}</a>
                <div class="drawer-toggle nav-button-animated w-nav-button" role="button" @click="$store.dispatch('nav/toggleSidebar')" data-w-id="cd8d589e-8a61-bc59-6d5c-1f13db2457d9"  style="-webkit-user-select: text;" aria-label="menu"  tabindex="0" aria-controls="w-nav-overlay-0" aria-haspopup="menu" aria-expanded="false">
                  <div data-w-id="cd8d589e-8a61-bc59-6d5c-1f13db2457da" class="top-line"></div>
                  <div data-w-id="cd8d589e-8a61-bc59-6d5c-1f13db2457db" class="middle-line"></div>
                  <div data-w-id="cd8d589e-8a61-bc59-6d5c-1f13db2457dc" class="bottom-line"></div>
                </div>
        </div>

        <div class="app-links">
            <app-links></app-links>
        </div>

    </header>
</template>

<script>
    import AppLinks from '~/components/appLinks'
export default {
    components: { AppLinks }
}
</script>

<style lang="scss" scoped>

.topMenu.home {
        background: imageUrl("logo.png") no-repeat center;
        background-size: contain;
        display: inline-block;
        padding: 0;
        cursor: pointer;
        height: $top_nav_height;
    }
    .actions-section{
      padding-right: 20px;
      text-align: right;
    }

    header{
        width:100%;
          position: fixed;
          top:0;
          display: grid;
          grid-template: $top_nav_height / auto 1fr;
          align-items: center;
          box-shadow: 1px 0 3px 2px rgb(0 0 0 / 4%);
      }


    .app-links{
        justify-self: end;
    }
    .brand-name {
        padding-left: 20px;
        font-size: 1.3rem;
    }
    .brand-name a {
        text-decoration: none;
        color: white;
    }
    .drawer-toggle .bar {
        width: 90%;
        height: 2px;
        background-color: $color-primary;
    }
    .drawer-toggle {
        display: inline-block;
        cursor: pointer;
    }
    header {
      background-color: #fff;
      z-index: 9999;
    }
    @media (max-width: 767px) {
      .topMenu.home {
          width:80px;
      }

        header:nth-child{
            justify-self: end !important;
        }
        .app-links {
            display: none;
        }
    }
    @media (min-width: 768px) {
      .topMenu.home {
        width:120px;
      }
        header{
            padding: 0 64px;
        }
        .app-links {
            display: block;
        }
        .drawer-toggle {
            display: none;
        }
    }
</style>
