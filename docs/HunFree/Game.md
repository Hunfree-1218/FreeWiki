# 훈프리 기록저장소

## HunFreeRun

* `첫 개시` - WebGame

<style>
  /* 1. MkDocs 테마 아이콘 크기 고정 */
  #game-section img {
    width: auto !important;
    height: auto !important;
    max-width: 50px; 
  }

  /* 2. 16:9 비율 유지를 위한 컨테이너 설정 (1920x1080 최적화) */
  .game-aspect-ratio-container {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%; /* 16:9 비율 (1080/1920 * 100) */
    height: 0;
    overflow: hidden;
    background: #000; /* 로딩 전 배경색 */
    border: 2px solid #ccc;
    border-radius: 8px;
    margin: 20px 0;
  }

  /* 3. iframe을 컨테이너에 꽉 채움 */
  .game-aspect-ratio-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
  }

  .game-info-text {
    text-align: center;
    color: #888;
    font-size: 0.9em;
  }
</style>

<section id="game-section">
    <h2>🎮 훈프리런 게임 플레이</h2>
    <div class="game-aspect-ratio-container">
        <iframe src="../../unity_assets/hunfreerun/index.html" 
                allowfullscreen>
        </iframe>
    </div>
    <p class="game-info-text">SpaceBar, Mouse1, 방향키로 점프 및 슬라이딩</p>


</section>

---
오른쪽아래 스크롤하면 전체화면있어요