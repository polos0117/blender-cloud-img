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

## 두 층 대미궁 — 2026-11-11

1024×3072 구조 자료. 위층 열 방과 섬, 아래층 도구 방 다섯, 연결 나선 계단과 입구.

- [구조 그림](img/2026-11-11_cave2-structure.png) · [선 그림](img/2026-11-11_cave2-lines.png) · [깊이](img/2026-11-11_cave2-depth.png)
- [방 색 지도](img/2026-11-11_cave2-ids.png) · [색 → 열쇠](img/2026-11-11_cave2-ids.json)
- [방 좌표와 등불 길](img/2026-11-11_cave2-rooms.json) · [보행 그래프](img/2026-11-11_cave2-nav.json)

보행 그래프: 319개 노드, 320개 양방향 간선. 입구에서 16개 장소 모두 도달 가능하며 간선마다 실제 보행면을 검사했다.
`scroll`은 문 앞에 들렀다가 되돌아오는 구간을 포함한 연속 경로이므로 노드가 반복된다.
Blender 5.2.4 LTS CPU, 64샘플: 구조 렌더 248.2초, 전체 생성 270.8초.
원본 씬은 코드 저장소의 `scenes/cave_hub2.blend`; 기존 한 층은 `--levels 1`로 재생성한다.
