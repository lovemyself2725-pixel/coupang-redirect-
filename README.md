# 쿠팡 바로가기 (홈 화면 앱 버튼)

폰 홈 화면에 아이콘을 하나 만들어서, 누르면 바로 내 쿠팡파트너스 링크를 거쳐 쿠팡으로 이동하게 해주는 페이지입니다.

## 1. GitHub Pages로 배포하기

1. GitHub 저장소 → **Settings → Pages**로 이동합니다.
2. **Source**를 "Deploy from a branch"로, **Branch**를 `main` / 폴더는 `/ (root)`로 선택하고 저장합니다.
3. 1~2분 후 `https://lovemyself2725-pixel.github.io/coupang-redirect-/` 주소가 생성됩니다. (Settings → Pages 화면에 정확한 주소가 표시됩니다.)

## 2. 폰에 앱 버튼으로 추가하기

받는 사람 폰에서 위 주소를 브라우저로 엽니다.

- **iPhone (Safari)**: 공유 버튼(⬆️) → "홈 화면에 추가"
- **Android (Chrome)**: 메뉴(⋮) → "홈 화면에 추가" 또는 "앱 설치"

홈 화면에 빨간 쇼핑백 아이콘이 생기고, 누르면 브라우저 주소창 없이 바로 쿠팡파트너스 링크로 이동한 뒤 쿠팡 앱/웹으로 연결됩니다.

## 3. 링크를 다른 상품으로 바꾸고 싶을 때

`index.html`을 열어 아래 두 곳의 URL을 원하는 쿠팡파트너스 링크로 바꾸면 됩니다.

```html
var COUPANG_PARTNERS_LINK = "https://link.coupang.com/a/새로운링크";
...
<meta http-equiv="refresh" content="0; url=https://link.coupang.com/a/새로운링크" />
```

저장 후 GitHub에 push하면 GitHub Pages가 자동으로 다시 배포합니다. 이미 홈 화면에 추가된 아이콘은 그대로 두면 되고, 다시 추가할 필요는 없습니다.
