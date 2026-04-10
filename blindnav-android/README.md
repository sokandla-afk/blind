# BlindNav 📍🔊

시각장애인을 위한 GPS 위치 안내 Android 앱

## 🚀 APK 빌드 방법 (GitHub Actions)

### 1단계 — 이 저장소를 GitHub에 올리기

```bash
# GitHub에서 새 저장소 생성 후:
git init
git add .
git commit -m "BlindNav 초기 커밋"
git remote add origin https://github.com/[내아이디]/blindnav.git
git push -u origin main
```

### 2단계 — 자동 빌드 확인

- GitHub 저장소 → **Actions** 탭 클릭
- `Build BlindNav APK` 워크플로가 자동 실행됨
- 약 5~10분 후 완료

### 3단계 — APK 다운로드

- Actions 탭 → 완료된 워크플로 클릭
- 하단 **Artifacts** → `BlindNav-debug` 다운로드
- 또는 **Releases** 탭에서 APK 다운로드

### 4단계 — 폰에 설치

1. 다운로드한 APK 파일을 폰으로 전송
2. **설정 → 보안 → 출처를 알 수 없는 앱** 허용
3. APK 탭하여 설치
4. 앱 실행 후 **위치 권한 허용**

## ✅ 주요 기능

- 📍 GPS 현재 위치 → 주소 음성 안내
- 🗺️ 주변 300m 내 장소 탐색 (음식점, 카페, 약국, 횡단보도 등)
- 🧭 나침반 방향 표시
- 🔊 한국어 TTS 음성 안내
- 📴 네이티브 앱 — file:// 위치권한 문제 없음

## 📁 프로젝트 구조

```
blindnav-android/
├── .github/workflows/build-apk.yml   ← 자동 APK 빌드
├── app/
│   └── src/main/
│       ├── assets/blindnav.html      ← 앱 UI (HTML/JS)
│       ├── java/.../MainActivity.java ← WebView + 위치권한 처리
│       └── AndroidManifest.xml
├── build.gradle
└── settings.gradle
```
