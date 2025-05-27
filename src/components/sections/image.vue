<script setup>
// GitHub raw URL for the image
const imgUrl =
  'https://raw.githubusercontent.com/sepermetric/sepermetric.github.io/main/src/components/mds/pipeline.png';
</script>

<template>
  <div>
    <!-- Section title -->
    <el-divider content-position="left">Pipeline</el-divider>

    <!-- Centered responsive image -->
    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12" class="text-center">
        <img :src="imgUrl" alt="Pipeline image" style="max-width: 100%;" />
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.text-center {
  text-align: center;
}
</style>
