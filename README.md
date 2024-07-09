## 프로젝트 개요:

본 프로젝트는 얼굴 인식 블러링 서비스를 개발하기 위한 초기 단계로, AI 모델 학습에 필요한 이미지를 수집하는 것을 목표로 합니다. 이를 위해 웹 크롤링을 통해 얼굴 이미지 데이터를 수집하고, 이를 로컬 저장소에 저장합니다.

## 주요 과정

### 1. 웹 크롤링 설정 및 초기화

- **Selenium 설정**: 크롤링을 위해 Selenium 웹 드라이버를 사용합니다. Chrome 브라우저를 헤드리스 모드로 실행하여 웹 페이지를 로드하고 스크롤합니다.
- **BeautifulSoup 사용**: 로드된 웹 페이지에서 HTML을 파싱하여 이미지 URL을 추출합니다.

### 2. 이미지 수집 및 저장

- **이미지 다운로드**: 추출된 이미지 URL을 통해 이미지를 다운로드합니다. 이미지가 특정 크기 이상일 경우에만 저장합니다.
- **로컬 저장소에 저장**: 다운로드한 이미지를 로컬 디렉토리에 저장합니다.

### 3. 스크롤 및 이미지 수집 반복

- **자동 스크롤**: 웹 페이지의 끝까지 스크롤하여 더 많은 이미지를 로드합니다. "더보기" 버튼이 있는 경우 이를 클릭하여 추가 이미지를 로드합니다.
- **이미지 수집 목표**: 5000개의 이미지를 수집할 때까지 이 과정을 반복합니다.
