# 훈프리 기록저장소

## 커맨더

* `첫 개시` - 웹 사이트 생성

# 훈프리 위키에 오신 것을 환영합니다!

이곳은 개발 과정에서 얻은 지식과 노하우를 기록하는 공간입니다  
현재 위키는 구축 중이며, 가끔 새로운 내용이 업데이트될 예정입니다  
좌측 메뉴를 통해 원하는 문서를 탐색해 보세요

## 💡 오늘의 마쉬멜로

둠피스트는 건틀릿을 낀채로 등을 긁을 수 없다

```
오늘살거 : 대파 2단, 멀록 정강이살 1근
```

<script src="https://www.gstatic.com/firebasejs/9.15.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.15.0/firebase-database-compat.js"></script>

<script>
  const firebaseConfig = {
    apiKey: "AIzaSyApq66dAZbTXSbQSBgNzaq5-DWHfyaXYR4", // 본인 것 확인
    authDomain: "hunfree-8ec0b.firebaseapp.com",
    projectId: "hunfree-8ec0b",
    storageBucket: "hunfree-8ec0b.firebasestorage.app",
    messagingSenderId: "1001768122486",
    appId: "1:1001768122486:web:e3bcaa3595106188850757",
    measurementId: "G-NGFS6XVC3T",
    // databaseURL은 아래 'Realtime Database' 메뉴에서 확인 가능한 주소입니다.
    databaseURL: "https://hunfree-8ec0b-default-rtdb.asia-southeast1.firebasedatabase.app" 
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.database();

  function getKstDateLabel() {
    const now = new Date();
    const kstNow = new Date(now.getTime() + (9 * 60 * 60 * 1000));
    let dateLabel = kstNow.toISOString().split('T')[0];
    if (kstNow.getHours() < 12) {
      const yesterday = new Date(kstNow.getTime() - (24 * 60 * 60 * 1000));
      dateLabel = yesterday.toISOString().split('T')[0];
    }
    return dateLabel;
  }

  const dateLabel = getKstDateLabel();
  const totalRef = db.ref('views/total');
  const dailyRef = db.ref('views/daily/' + dateLabel);

  totalRef.transaction(c => (c || 0) + 1);
  dailyRef.transaction(c => (c || 0) + 1);

  totalRef.on('value', s => document.getElementById('total-views').innerText = s.val());
  dailyRef.on('value', s => document.getElementById('daily-views').innerText = s.val() || 1);
</script>