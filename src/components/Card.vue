<template>
  <at-card :style="{ width: '300px' }">
    <h4 slot="title">Card Title</h4>
    <div slot="extra"><a>Extra</a></div>
    <div>
      Card Content
    </div>
  </at-card>
</template>

<script>
export default {
  name: 'Card',
};
</script>
