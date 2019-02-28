<template>
  <div class="menu-items" @click="closeMenu">
    <nuxt-link v-for="item, i in items"
    v-touchfeedback :key="i" :to="item.to" class="menu-item">

      {{ item.label }}
    </nuxt-link>
  </div>


</template>

<script>
import { mapMutations } from 'vuex'

export default {
    data() {
        return {
            items: [
                { to: '/', label: 'Dashboard' },
                { to: { name: 'profile' }, label: 'Profile' }
            ]
        }
    },

    methods: {
        ...mapMutations({
            closeMenu: 'ui/closeMenu',
        })
    },
}
</script>

<style>
.menu-items { padding: 20px; }

.menu-item {
    color: #F7F7F7;
    display:       block;
    margin-bottom: 20px;
    font-weight:     bold;
    text-decoration: none;
}
.menu-item:hover, .menu-item.is-touch { color: #AEAEAE; }

.menu-item.nuxt-link-exact-active { color: #FF5D25; }
</style>
