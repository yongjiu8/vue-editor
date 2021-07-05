<template>
    <div class="box-home">
        <div
            v-for="(it, index) in formData.texts"
            :key="index"
            class="item"
        >
            {{ index + '：' + it }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'TextGrideView',
    props: {
        formData: {
            type: Object,
            default: () => ({})
        }
    }
};
</script>

<style lang="css" scoped>
.box-home {
  width: 100%;
  height: 300px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-items: center;
  justify-content: space-evenly;
  align-items: center;
  align-content: space-evenly;
}
.item {
  width: 26%;
  height: 50px;
  text-align: center;
  line-height: 50px;
  vertical-align: middle;
  font-size: 30px;
  color: #999999;
  border: 1px solid orange;
}
</style>
