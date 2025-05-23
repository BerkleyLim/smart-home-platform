# smart-home-platform
node.js 환경에서 smart-home-platform 사용


## 디렉토리 구조

```
smart-home/
├── client/                # React 앱
│   ├── public/
│   ├── src/
│   └── build/             # 빌드 결과물 (Express가 서빙)
├── server/                # Express.js 서버
│   ├── routes/
│   │   ├── oauth.js
│   │   ├── fulfillment.js
│   │   └── smartthings.js
│   ├── views/             # login.html (Google OAuth 용)
│   └── server.js
├── package.json           # 루트에서 의존성 통합 관리
```

## 핵심 흐름

1.	사용자가 Google Home 앱에서 기기 연동
2.	Google → /oauth/authorize → 로그인 화면 (React 또는 login.html)
3.	로그인 → /oauth/token → 토큰 발급
4.	Google → /smarthome → Fulfillment intent 처리
5.	/api/smartthings → SmartThings API 호출
6.	React 앱은 /dashboard, /logout 등 제공


## 실행 흐름

```bash
# React 앱 빌드
cd client
npm run build

# Express 서버 실행 (React 포함)
cd ../server
node server.js
```

