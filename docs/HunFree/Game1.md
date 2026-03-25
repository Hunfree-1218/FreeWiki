# 훈프리 기록저장소

## Next Plan

* `프리런` - 다음 프로젝트: 런게임 개발기

<style>
  /* 갤러리 레이아웃 설정 */
  .gallery-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* 한 줄에 2개 배치 */
    gap: 15px;
    margin: 20px 0;
  }
  .gallery-item {
    text-align: center;
  }
  .gallery-item img {
    width: 100%;
    border-radius: 8px;
    border: 1px solid #333; /* 다크 테마에 어울리는 테두리 */
    box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    transition: transform 0.2s;
  }
  .gallery-item img:hover {
    transform: scale(1.03); /* 마우스 올리면 살짝 커지는 효과 */
  }
  .image-caption {
    margin-top: 8px;
    font-size: 0.85em;
    color: #aaa;
  }
</style>

### 📸 개발 스크린샷 갤러리

<div class="gallery-container">
  <div class="gallery-item">
    <img src="../../Image/FreeRunTitle.jpg" alt="Title Screen">
    <div class="image-caption">1. 메인 타이틀 화면</div>
  </div>
  <div class="gallery-item">
    <img src="../../Image/FreeRun1.jpg" alt="Level Design">
    <div class="image-caption">2. 캐릭터 설정 및 맵 구성</div>
  </div>
  <div class="gallery-item">
    <img src="../../Image/FreeRunInGameDead.jpg" alt="In-game Death Check">
    <div class="image-caption">3. 인게임 사망 판정 테스트</div>
  </div>
  <div class="gallery-item">
    <img src="../../Image/FreeRunInGame.jpg" alt="Gameplay">
    <div class="image-caption">4. 실제 게임 플레이 화면</div>
  </div>
  <div class="gallery-item">
    <img src="../../Image/FreeRunDead.jpg" alt="Death Scene">
    <div class="image-caption">5. 데드 씬 연출</div>
  </div>
  <div class="gallery-item">
    <img src="../../Image/FreeRunEND.png" alt="End Screen">
    <div class="image-caption">6. 게임 종료 및 결과 창</div>
  </div>
</div>

---

### 📝 개발 노트
위 이미지는 AI 생성물이 아닌 **'훈프리'**의 개인 도트 작업물입니다.
본 프로젝트는 유니티 WebGL 환경에 최적화되어 개발 중입니다.