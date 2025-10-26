<template>
  <v-footer
    app
    height="80"
    class="custom-footer"
  >
    <a
      v-for="item in items"
      :key="item.title"
      class="d-inline-block mx-2 social-link"
      :href="item.href"
      rel="noopener noreferrer"
      target="_blank"
      :title="item.title"
    >
      <v-icon
        :icon="item.icon"
        :size="item.icon === '$vuetify' ? 24 : 16"
      />
    </a>

    <div
      class="text-caption footer-text"
      style="position: absolute; right: 16px;"
    >
      &copy; 2016-{{ (new Date()).getFullYear() }} <span class="d-none d-sm-inline-block">Institución Educativa Comfacor</span>
      —
      <a
        class="text-decoration-none license-link"
        href="https://vuetifyjs.com/about/licensing/"
        rel="noopener noreferrer"
        target="_blank"
      >
        Políticas de Privacidad
      </a>
    </div>
  </v-footer>
</template>

<script setup>
  const items = [
    {
      title: 'Facebook',
      icon: 'mdi-facebook',
      href: '#',
    },
    {
      title: 'Instagram',
      icon: 'mdi-instagram',
      href: '#',
    },
    {
      title: 'Twitter',
      icon: 'mdi-twitter',
      href: '#',
    },
    {
      title: 'YouTube',
      icon: 'mdi-youtube',
      href: '#',
    },
    {
      title: 'Email',
      icon: 'mdi-email',
      href: '#',
    },
  ]
</script>

<style scoped lang="sass">
.custom-footer
  background: linear-gradient(135deg, #e3f2fd 0%, #f5fbff 100%) !important
  border-top: 3px solid #b3e5fc !important
  box-shadow: 0 -4px 12px rgba(179, 229, 252, 0.3) !important

.footer-text
  color: #01579b !important

.license-link
  color: #0277bd !important
  transition: color 0.3s ease

  &:hover
    color: #01579b !important

.social-link :deep(.v-icon)
  color: #0277bd
  text-decoration: none
  transition: all 0.3s ease-in-out
  padding: 8px
  border-radius: 50%
  background: rgba(255, 255, 255, 0.7)

  &:hover
    color: #01579b
    background: rgba(255, 255, 255, 0.9)
    transform: translateY(-2px)
    box-shadow: 0 4px 8px rgba(2, 119, 189, 0.2)
</style>