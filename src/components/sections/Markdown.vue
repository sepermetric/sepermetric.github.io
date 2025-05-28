<script setup>
import page from '../mds/md.mdx';
import pipelinepage from '../mds/pipelinemd.mdx';
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
            <page />
        </el-col>
    </el-row>

    <el-divider />
    
      <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
            <pipelinepage />
        </el-col>
    </el-row>

  </div>
</template>
