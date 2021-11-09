<template>
    <div>
      <TileRadioButton
        v-model="radio"
        name="personal-list-radio"
        :options="options"
        title="個人リストやり取り方法"
      ></TileRadioButton>
    </div>
</template>

<script>
import TileRadioButton from './components/TileRadioButton.vue'

export default {
  components: {
    TileRadioButton
  },
  data () {
    return {
      radio: null,
      options: [
        { label: 'オンライン', value: 0 },
        { label: 'JMDCオンライン', value: 1 },
        { label: 'メール', value: 2 },
        { label: '双方媒体', value: 3 },
        { label: '健保からのみ媒体', value: 4 }
      ]
    }
  }
}
</script>

<style scoped>
p{
  color: green
}
</style>
