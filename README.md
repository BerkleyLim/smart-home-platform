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
