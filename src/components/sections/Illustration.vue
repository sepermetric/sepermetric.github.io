<template>
  <div class="illustration-section">
    <el-row justify="center">
      <el-col :span="22">
        <h2 class="section-title">Illustration</h2>
        <div class="illustration-container">
          <el-image 
            :src="gifPath" 
            fit="contain"
            class="illustration-gif"
            :lazy="true"
            :preview-src-list="[gifPath]"
          >
            <template #error>
              <div class="image-error">
                <el-icon><Picture /></el-icon>
                <span>Failed to load illustration</span>
              </div>
            </template>
          </el-image>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { Picture } from '@element-plus/icons-vue'

export default {
  name: 'Illustration',
  components: {
    Picture
  },
  data() {
    return {
      gifPath: '/seper_slides.gif'
    }
  }
}
</script>

<style scoped>
.illustration-section {
  margin: 40px 0;
  padding: 20px 0;
}

.section-title {
  font-family: "MyFont", Verdana, sans-serif;
  font-size: 32px;
  font-weight: bold;
  text-align: center;
  margin-bottom: 30px;
  color: #2c3e50;
  letter-spacing: 1px;
}

.illustration-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  max-width: 100%;
}

.illustration-gif {
  max-width: 45%;
  max-height: 300px;
  width: auto;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  border: 2px solid #f0f0f0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.illustration-gif:hover {
  transform: scale(1.02);
  box-shadow: 0 12px 48px rgba(0, 0, 0, 0.15);
}

.image-error {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 200px;
  color: #909399;
  background-color: #f5f7fa;
  border-radius: 10px;
}

.image-error span {
  margin-top: 10px;
  font-size: 14px;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .illustration-gif {
    max-width: 47.5%;
    max-height: 200px;
  }
  
  .section-title {
    font-size: 28px;
  }
}

@media (max-width: 480px) {
  .illustration-gif {
    max-width: 50%;
    max-height: 150px;
  }
  
  .section-title {
    font-size: 24px;
  }
}
</style>
