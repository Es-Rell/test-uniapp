<template>
  <view v-if="!noHeight" />
  <view class="header" :style="{ color, background }">
    <view>
      <template v-if="isBack">
        <uni-icons type="left" :color="color" size="22" @click="navigateBack" />
      </template>
      <slot name="left" />
    </view>
    <view class="center"><slot /></view>
  </view>
</template>

<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    isBack?: boolean;
    color?: string;
    background?: string;
    noHeight: boolean;
  }>(),
  {
    isBack: false,
    color: "#333",
    background: "#fff",
    noHeight: false,
  }
);

const navigateBack = () => uni.navigateBack({ delta: 1 });
</script>

<style lang="scss" scoped>
.header {
  padding: 0 30rpx;
  font-size: 30rpx;
  display: flex;
  align-items: center;
  z-index: 1001;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  .center {
    position: absolute;
    width: 400rpx;
    left: 50%;
    margin-left: -200rpx;
    text-align: center;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
}
</style>
