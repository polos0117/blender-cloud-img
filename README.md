# blender-cloud-img

[blender-cloud](https://github.com/polos0117/blender-cloud) 의 그림 저장소. 코드 저장소가 무거워지지 않게 결과물은 여기 둔다 — Pages 로 `https://polos0117.github.io/blender-cloud-img/img/<파일>` 에서 읽는다.

## 자리

```
img/<날짜>_<이름>.<확장자>     결과물. 날짜(YYYY-MM-DD)를 앞에 붙이면 갤러리에서 새것이 위로 온다
```

갤러리(https://polos0117.github.io/blender-cloud/)는 `img/` 를 GitHub API 로 읽어 그대로 보여 준다 — 목록 파일은 없다.

| 종류 | 확장자 | 웹용 권장 |
|---|---|---|
| 이미지 | png · webp · jpg | 투명 배경 PNG/WebP, 화면 폭의 2배 |
| 영상 | webm · mp4 | 2~4초 루프, 1MB 안팎. iPhone Safari 는 투명 WebM 을 못 튼다 |
| 3D 모델 | glb | 압축(Draco/meshopt), 1MB 이하 |

.blend 원본은 코드 저장소 `scenes/` 에 둔다. Pages 사이트 한 개는 1 GB 까지다 — 차면 `blender-cloud-img-2` 를 만든다.
