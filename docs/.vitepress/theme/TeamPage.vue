<template>
  <div class="team-page-wrapper">
    <div class="team-content">
      <div class="team-grid">
        <div
          v-for="(member, index) in teamMembers"
          :key="member.name"
          class="team-card-wrapper"
          :style="{ animationDelay: `${index * 0.1 + 0.1}s` }"
        >
          <a
            :href="member.github"
            target="_blank"
            class="team-card"
          >
            <div class="card-content">
              <!-- 装饰元素 -->
              <div class="card-decorations">
                <div class="paw-print paw-1">
                  <div class="paw-pad"></div>
                  <div class="paw-toes">
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                  </div>
                </div>
                <div class="paw-print paw-2">
                  <div class="paw-pad"></div>
                  <div class="paw-toes">
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                  </div>
                </div>
                <div class="paw-print paw-3">
                  <div class="paw-pad"></div>
                  <div class="paw-toes">
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                    <div class="toe"></div>
                  </div>
                </div>
                <div class="sparkle sparkle-1">✨</div>
                <div class="sparkle sparkle-3">⭐</div>
                <div class="code-symbol">{}</div>
              </div>

              <!-- 头像 -->
              <div class="avatar-container">
                <img
                  :src="member.avatar"
                  :alt="member.name"
                  class="avatar"
                />
                <!-- 头像装饰光环 -->
                <div class="avatar-decoration">
                  <div class="glow-ring"></div>
                  <div class="floating-dots">
                    <div class="dot dot-1"></div>
                    <div class="dot dot-2"></div>
                    <div class="dot dot-3"></div>
                  </div>
                </div>
              </div>

              <!-- 信息内容 -->
              <div class="member-info">
                <h3 class="member-name">{{ member.name }}</h3>
                <p class="member-role">{{ member.role }}</p>
                <div class="role-divider"></div>
                <p class="member-description">{{ member.description }}</p>
              </div>

              <!-- GitHub 图标 -->
              <div class="github-icon">
                <svg width="30" height="30" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z" />
                </svg>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const teamMembers = ref([
  {
    name: '钦灵',
    role: '项目负责人',
    description: '开发群友性功能',
    avatar: 'https://avatars.githubusercontent.com/u/85441945',
    github: 'https://github.com/SlimeBoyOwO'
  },
  {
    name: 'Skylar_luna (七辰)',
    role: '客服',
    description: '给新成员榨干！',
    avatar: 'https://avatars.githubusercontent.com/u/162135575',
    github: 'https://github.com/qichenya'
  },
  {
    name: '风雪大人',
    role: '全栈功能开发 / 项目发展规划',
    description: '一只喜欢趴在键盘上睡觉的蓝色的猫，翻身压到的键盘字母恰巧是LingChat新功能的代码',
    avatar: 'https://avatars.githubusercontent.com/u/183904010',
    github: 'https://github.com/T-Auto'
  },
  {
    name: '雅诺狐',
    role: 'WIKI负责人',
    description: '普普通通的维基狐一枚，喜欢毛茸茸的小fox',
    avatar: 'https://avatars.githubusercontent.com/u/212194964',
    github: 'https://github.com/foxcyber907'
  },
  {
    name: '影空',
    role: '文档编写和Bug修复',
    description: '只想摸鱼的废柴一个',
    avatar: 'https://avatars.githubusercontent.com/u/141255649',
    github: 'https://github.com/shadow01a'
  },
  {
    name: '鲸落',
    role: 'RAG架构',
    description: '云，二次元和ai爱好者',
    avatar: 'https://avatars.githubusercontent.com/u/84253913',
    github: 'https://github.com/LtePrince'
  }
])
</script>

<style scoped>
.team-page-wrapper {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--vp-c-bg, #ffffff);
  z-index: 1;
  overflow-y: auto;
  padding-top: 60px;
  animation: pageSlideIn 0.8s ease-out;
}

@keyframes pageSlideIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.team-content {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 1.5rem;
  justify-items: center;
}

.team-card-wrapper {
  width: 100%;
  max-width: 500px;
  opacity: 1;
  animation: cardSlideUp 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
}

@keyframes cardSlideUp {
  from {
    transform: translateY(30px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

.team-card {
  display: block;
  background: var(--vp-c-bg-soft, #f6f6f7);
  border-radius: 16px;
  padding: 1.5rem;
  text-decoration: none;
  color: inherit;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow:
    0 4px 16px rgba(0, 0, 0, 0.08),
    0 2px 8px rgba(0, 0, 0, 0.04);
  border: 1px solid var(--vp-c-divider, #e2e2e3);
  height: 100%;
  position: relative;
  overflow: hidden;
}

.team-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(25, 118, 210, 0.03), rgba(66, 165, 245, 0.03));
  opacity: 0;
  transition: opacity 0.3s ease;
  border-radius: 16px;
}

.team-card:hover {
  transform: translateY(-4px) scale(1.01);
  box-shadow:
    0 12px 24px rgba(0, 0, 0, 0.12),
    0 6px 12px rgba(25, 118, 210, 0.08);
  border-color: rgba(25, 118, 210, 0.3);
}

.team-card:hover::before {
  opacity: 1;
}

/* 装饰元素样式 */
.card-decorations {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  pointer-events: none;
  z-index: 0;
}

/* 猫爪印样式 - 从右下角开始，更大尺寸 */
.paw-print {
  position: absolute;
  opacity: 0.2;
  transition: all 0.4s ease;
  transform-origin: center;
}

.paw-1 {
  bottom: 15px;
  right: 20px;
  transform: rotate(-25deg) scale(1.8);
}

.paw-2 {
  bottom: 50px;
  right: 55px;
  transform: rotate(10deg) scale(1.4);
}

.paw-3 {
  bottom: 80px;
  right: 25px;
  transform: rotate(-15deg) scale(1.2);
}

.team-card:hover .paw-print {
  opacity: 0.45;
}

.team-card:hover .paw-1 {
  transform: rotate(-20deg) scale(1.9);
}

.team-card:hover .paw-2 {
  transform: rotate(15deg) scale(1.5);
}

.team-card:hover .paw-3 {
  transform: rotate(-10deg) scale(1.3);
}

.paw-pad {
  width: 18px;
  height: 16px;
  background: #1976D2;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
  margin: 0 auto 4px;
}

.paw-toes {
  display: flex;
  justify-content: space-between;
  width: 24px;
  margin: 0 auto;
}

.toe {
  width: 5px;
  height: 6px;
  background: #1976D2;
  border-radius: 50%;
}

/* 闪光效果 */
.sparkle {
  position: absolute;
  font-size: 10px;
  opacity: 0.5;
  animation: sparkleFloat 3s ease-in-out infinite;
}

.sparkle-1 {
  top: 20%;
  left: 15%;
  animation-delay: 0s;
}

.sparkle-2 {
  top: 60%;
  left: 25%;
  animation-delay: 1s;
}

.sparkle-3 {
  top: 35%;
  left: 10%;
  animation-delay: 2s;
}

@keyframes sparkleFloat {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
    opacity: 0.5;
  }
  50% {
    transform: translateY(-8px) rotate(180deg);
    opacity: 0.9;
  }
}

/* 代码符号装饰 */
.code-symbol {
  position: absolute;
  top: 50%;
  right: 10px;
  font-family: 'Courier New', monospace;
  font-size: 28px;
  color: #1976D2;
  opacity: 0.06;
  transform: translateY(-50%);
  transition: all 0.3s ease;
}

.team-card:hover .code-symbol {
  opacity: 0.18;
  transform: translateY(-50%) scale(1.1);
}

.card-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 100%;
  min-height: 120px;
  position: relative;
  z-index: 1;
  gap: 1.5rem;
}

.avatar-container {
  flex-shrink: 0;
  position: relative;
}

/* 头像装饰 */
.avatar-decoration {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  pointer-events: none;
}

.glow-ring {
  position: absolute;
  width: 90px;
  height: 90px;
  border: 2px solid rgba(25, 118, 210, 0.2);
  border-radius: 50%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: all 0.4s ease;
  animation: pulse 2s ease-in-out infinite;
}

.team-card:hover .glow-ring {
  opacity: 1;
  transform: translate(-50%, -50%) scale(1.1);
}

@keyframes pulse {
  0%, 100% {
    transform: translate(-50%, -50%) scale(1);
  }
  50% {
    transform: translate(-50%, -50%) scale(1.05);
  }
}

.floating-dots {
  position: absolute;
  width: 100px;
  height: 100px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.dot {
  position: absolute;
  width: 4px;
  height: 4px;
  background: #42A5F5;
  border-radius: 50%;
  opacity: 0;
  transition: all 0.4s ease;
}

.dot-1 {
  top: 10px;
  left: 50%;
  transform: translateX(-50%);
}

.dot-2 {
  bottom: 10px;
  left: 20px;
}

.dot-3 {
  bottom: 10px;
  right: 20px;
}

.team-card:hover .dot {
  opacity: 0.8;
  animation: floatDot 2s ease-in-out infinite;
}

@keyframes floatDot {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-3px);
  }
}

.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid #1976D2;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 4px 12px rgba(25, 118, 210, 0.15);
  position: relative;
  z-index: 2;
}

.team-card:hover .avatar {
  transform: scale(1.06) rotate(3deg);
  border-color: #42A5F5;
  box-shadow: 0 6px 16px rgba(25, 118, 210, 0.25);
}

.member-info {
  flex: 1;
  text-align: left;
  margin-bottom: 0;
}

.member-name {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--vp-c-text-1, #213547);
  margin: 0 0 0.25rem 0;
  transition: all 0.3s ease;
}

.team-card:hover .member-name {
  color: #1976D2;
  transform: translateX(2px);
}

.member-role {
  font-size: 0.9rem;
  color: var(--vp-c-text-2, #476582);
  margin: 0 0 0.5rem 0;
  font-weight: 500;
  transition: all 0.3s ease;
}

.team-card:hover .member-role {
  color: #42A5F5;
  transform: translateX(2px);
}

.role-divider {
  width: 40px;
  height: 2px;
  background: linear-gradient(90deg, #1976D2, #42A5F5);
  margin: 0 0 0.5rem 0;
  border-radius: 1px;
  transition: all 0.3s ease;
}

.team-card:hover .role-divider {
  width: 60px;
  background: linear-gradient(90deg, #42A5F5, #1976D2, #42A5F5);
}

.member-description {
  font-size: 0.8rem;
  color: var(--vp-c-text-2, #476582);
  line-height: 1.4;
  margin: 0;
  transition: all 0.3s ease;
}

.team-card:hover .member-description {
  color: var(--vp-c-text-1, #213547);
  transform: translateX(2px);
}

.github-icon {
  flex-shrink: 0;
  color: var(--vp-c-text-3, #959595);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  transform-origin: center;
  align-self: flex-end;
}

.team-card:hover .github-icon {
  color: #1976D2;
  transform: scale(1.1) rotate(15deg);
}

/* 响应式设计 */
@media (max-width: 768px) {
  .team-content {
    padding: 1rem;
  }

  .team-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .team-card {
    padding: 1rem;
    border-radius: 12px;
  }

  .card-content {
    gap: 1rem;
    min-height: 100px;
  }

  .avatar {
    width: 60px;
    height: 60px;
  }

  .glow-ring {
    width: 70px;
    height: 70px;
  }

  .member-name {
    font-size: 1.1rem;
  }

  .member-role {
    font-size: 0.85rem;
  }

  .member-description {
    font-size: 0.75rem;
  }

  .paw-print {
    transform: scale(0.9);
  }

  .sparkle {
    font-size: 8px;
  }
}

@media (max-width: 480px) {
  .team-page-wrapper {
    padding-top: 50px;
  }

  .team-grid {
    grid-template-columns: 1fr;
  }

  .card-content {
    flex-direction: column;
    text-align: center;
    gap: 1rem;
  }

  .member-info {
    text-align: center;
  }

  .role-divider {
    margin: 0 auto 0.5rem auto;
  }

  .github-icon {
    align-self: center;
  }

  .card-decorations {
    opacity: 0.6;
  }
}

@media (prefers-reduced-motion: reduce) {
  .team-page-wrapper,
  .team-card-wrapper {
    animation: none;
  }

  .sparkle,
  .glow-ring,
  .dot {
    animation: none;
  }

  .team-card,
  .avatar,
  .member-name,
  .member-role,
  .role-divider,
  .member-description,
  .github-icon {
    transition: opacity 0.2s ease;
  }

  .team-card:hover {
    transform: none;
    opacity: 0.9;
  }

  .team-card:hover .avatar,
  .team-card:hover .member-name,
  .team-card:hover .member-role,
  .team-card:hover .member-description,
  .team-card:hover .github-icon {
    transform: none;
  }
}
</style>
