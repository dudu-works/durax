# durax

`dudu`의 `hyrax`, `durax`입니다. 평범하고 실제 동물처럼 생긴 바위너구리 Codex pet입니다.

귀여운 캐릭터나 일러스트가 아니라 짧고 둥근 실제 바위너구리의 생김새를 유지했습니다. 입을 벌리는 동작에서는 작은 앞니가 보이고, 대기 동작에서는 혀를 짧게 내밉니다.

![Idle animation](preview/idle.gif)

## 특징

- Codex pet sprite version 2
- 8열 11행, 1536 x 2288 WebP spritesheet
- idle 동작 뒤에 같은 기본 자세로 복귀
- 작은 앞니와 혀 동작
- 검정색과 흰색 배경에서 모두 보이는 이중 외곽선
- 모든 프레임에 최소 9px 투명 여백

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

![Waiting animation](preview/waiting.gif)

![Running animation](preview/running.gif)

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
- 사용된 74개 셀의 최소 여백 9px
