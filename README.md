# durax

`dudu`의 `hyrax`, `durax`입니다. 평범하고 실제 동물처럼 생긴 바위너구리 Codex pet입니다.

귀여운 캐릭터나 일러스트가 아니라 짧고 둥근 실제 바위너구리의 생김새를 유지했습니다. 입을 벌리는 동작에서는 작은 앞니가 보이고, 납작하게 앉은 동작에서는 몸을 고정한 채 눈에 보이는 짧은 혀를 내밀고 있습니다.

마우스를 올리면 idle과 가까운 반기립 착석 자세에서 얼굴을 화면 중심에서 살짝 비껴난 3/4 정면으로 돌리고 `아와왁!!` 합니다. 가까운 눈이 더 크게 보이지만 두 동공은 화면을 붙잡고, 긴장된 눈매와 볼, 입꼬리로 작은 들숨 뒤 두 번 강하게 발화합니다. hover 뒤에는 자연스러운 짧고 넓은 비율로 쪼그린 채 혀 길이만 왕복합니다.

![Idle animation](preview/idle.gif)

## 특징

- Codex pet sprite version 2
- 8열 11행, 1536 x 2288 WebP spritesheet
- idle 동작 뒤에 같은 기본 자세로 복귀
- idle 안에서 왼쪽 기본, 위, 왼쪽 기본, 아래 시선을 보여주는 동작
- 마우스 hover 시 `작은 아 - 조금 큰 아 - 큰 와! - 중간 회수 - 최대 왁!!`의 5프레임 호흡 루프
- 측면 프로필이나 정중앙 대칭이 아닌 비껴난 3/4 정면과 한쪽 우세 시선
- 실제 동물의 눈썹뼈, 눈매, 볼과 입꼬리 긴장으로 표독스러운 발화 강도 표현
- idle과 발 기준선을 맞춘 반기립 착석 자세로 hover 전환 격차 축소
- 코끝과 머리 깊이를 고정하고 볼과 입꼬리만 넓혀 뾰족한 주둥이 돌출 방지
- hover 뒤 와와 발성 없이 쪼그린 채 혀 길이만 짧음과 중간 사이로 왕복하는 동작
- 작은 앞니와 이전 혀 끝보다 약 2배 긴 혀 동작
- 한 번 납작하게 앉은 뒤 몸 변화 없이 혀 길이를 고정하는 동작
- 오른쪽과 왼쪽 달리기의 크기와 발 기준선 일치
- 검정색과 흰색 배경에서 모두 보이는 이중 외곽선
- 모든 행에 원본 중복 테두리 없이 동일한 흰색 안쪽선과 검정 바깥선 적용
- 모든 프레임에 최소 8px 투명 여백

## 설치

macOS 또는 Linux 터미널에서 다음 명령을 실행합니다.

```sh
git clone https://github.com/dudu-works/durax.git
mkdir -p ~/.codex/pets/durax
cp durax/pet.json ~/.codex/pets/durax/pet.json
cp durax/spritesheet.webp ~/.codex/pets/durax/spritesheet.webp
```

그다음 Codex에서 pet을 `durax`로 선택합니다. 이미 Codex가 실행 중이라면 앱을 다시 시작합니다.

## 미리보기

### 전체 동작 프레임

![Contact sheet](preview/contact-sheet.png)

### 검정색과 흰색 배경 대비

![Outline contrast](preview/outline-contrast.png)

### 입과 혀 동작

마우스 hover:

![Hover shout animation](preview/hover-shout.gif)

hover 후 쪼그린 채 혀 길이 왕복:

![Ready shout animation](preview/ready-shout.gif)

납작하게 앉아 짧은 혀 끝 내밀기:

![Flat tongue animation](preview/failed-tongue.gif)

![Waiting animation](preview/waiting.gif)

![Running animation](preview/running.gif)

좌우 달리기 크기 비교:

![Running right animation](preview/running-right.gif)

![Running left animation](preview/running-left.gif)

## 파일

- `pet.json` - Codex pet 메타데이터
- `spritesheet.webp` - 설치용 최종 spritesheet
- `preview/` - 동작과 외곽선 미리보기
- `qa/validation.json` - spritesheet 형식 검증 결과
- `qa/outline-report.json` - 셀 안전 여백 검증 결과

## 검증 상태

- atlas 오류 0건
- atlas 경고 0건
- 투명 픽셀 RGB 잔여 0개
- 사용된 74개 셀의 최소 여백 8px
