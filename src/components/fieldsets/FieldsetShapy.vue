<template>
  <div class="fieldset fieldset-shapy">
    <!-- TITLE & DESCRIPTION -->
    <h1 class="legend title-legend">{{ title }}</h1>
    <group-toggle :hidden="hidden" @click.native="hidden = !hidden" />
    <template v-if="!hidden">
      <p class="desc">{{ desc }}</p>
    </template>
  </div>
</template>

<script>
import GroupToggle from '@/components/GroupToggle'
export default {
  name: 'Shapy',
  components: {
    GroupToggle
  },
  data: () => ({
    hidden: false,
    title: 'Gradient Generator',
    desc:
      'A CSS gradient generator based on Shapy.',
  })
}
</script>

<style lang="sass" scoped>

.title-legend
  font-size: 1.5em

.social-list
  display: flex
  list-style-type: none
  align-items: center
  width: 100%
  flex-wrap: wrap

.social-item
  font-size: .93em
  font-weight: 500
  display: flex
  align-items: center
  margin-right: 1em
  margin-top: .5em

.social-icon
  font-size: 1em
  margin-right: .3em
</style>
