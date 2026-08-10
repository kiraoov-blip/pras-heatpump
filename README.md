# 제주 히트펌프 요금분석 시뮬레이터

GitHub Pages에서 바로 실행할 수 있는 정적 웹페이지입니다.

## 업로드할 파일

실행에 반드시 필요한 파일은 `index.html` 하나입니다.  
`.nojekyll`은 GitHub Pages가 파일을 그대로 배포하도록 돕는 보조 파일입니다.

- `index.html` : 시뮬레이터 본체 + 분석 데이터 내장
- `.nojekyll` : GitHub Pages 보조 파일
- `README.md` : 배포 및 사용 설명서(사이트 작동에는 불필요)

## 중요: 데이터 공개 범위

원 고객번호는 `HP01`~`HP16`으로 익명화했습니다. 다만 시뮬레이터 계산을 위해 시간대별 전력사용량 데이터가 `index.html` 내부에 포함되어 있습니다. 일반 공개 GitHub Pages를 사용하면 이 데이터도 기술적으로 외부에서 열람할 수 있습니다. 민감한 실측 데이터라면 공개 배포 전에 조직의 보안 기준을 확인하세요.

## GitHub Pages 배포 절차

1. GitHub에서 새 Repository를 생성합니다. 예: `jeju-heatpump-tariff`
2. Repository의 **Add file → Upload files**를 선택합니다.
3. 이 폴더의 `index.html`, `.nojekyll`, `README.md`를 업로드하고 **Commit changes**를 누릅니다.
4. Repository 상단 **Settings**로 이동합니다.
5. 왼쪽 메뉴 **Pages**를 선택합니다.
6. **Build and deployment → Source**에서 `Deploy from a branch`를 선택합니다.
7. Branch는 `main`, Folder는 `/(root)`를 선택한 후 **Save**합니다.
8. Pages 설정 화면에 표시되는 사이트 주소로 접속합니다.

## 기존 Repository에 올리는 경우

기존 GitHub Pages 저장소를 쓰는 경우, 현재 사이트 파일을 보관한 뒤 이 `index.html`을 저장소 루트의 `index.html`로 교체하면 됩니다. 같은 이름의 파일이 이미 있으면 덮어쓰게 됩니다.

## 수정 시 주의사항

- 기본 옥토퍼스형 할인율: 51%
- 기본 인상률: 50%
- 할인시간: 04~07시, 13~16시, 22~24시
- 인상시간: 16~22시
- 부하이전: 현재 버전에서는 미적용
- 비용 범위: 전력량요금만 비교
- 요금 기준: 2026년 현행 요금표

향후 부하이전 기능을 추가할 때는 `index.html`만 교체해도 동일한 GitHub Pages 주소를 계속 사용할 수 있습니다.
