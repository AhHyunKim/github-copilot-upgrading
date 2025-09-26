# upgraded 폴더 파일 구조 및 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일 및 디렉터리 구조를 그대로 복사하여, 최신 Python 환경에서 리팩토링 및 업그레이드 작업을 진행하는 공간입니다.

## 최상위 파일 및 폴더
- MANIFEST.in: 패키징 시 포함할 파일 목록을 지정하는 설정 파일
- README.rst: 프로젝트 및 설정 관리자인 Guachi에 대한 설명 문서
- distribute-0.6.10.tar.gz: 레거시 Python 패키징 도구인 distribute의 압축 파일
- distribute_setup.py: distribute 설치 스크립트
- setup.py: 프로젝트 설치 및 배포를 위한 Python 스크립트
- docs/: 프로젝트 문서 및 Sphinx 기반 빌드 결과물 폴더
- guachi/: 핵심 Python 모듈 및 설정 관리 기능 구현 폴더
- guachi.egg-info/: 패키징 정보 및 메타데이터 폴더

## docs/ 하위 구조
- Makefile: Sphinx 문서 빌드용 Makefile
- build/: Sphinx로 빌드된 문서 결과물
  - doctrees/: Sphinx 내부 문서 트리 및 캐시 파일
  - html/: HTML 문서 결과물
    - _sources/: 각 문서의 원본 텍스트 파일
    - _static/: CSS, JS 등 정적 리소스 파일
- source/: Sphinx 문서 원본
  - changelog.rst, example_usage.rst, getting_started.rst, index.rst, other_uses.rst: 각종 문서 원본
  - _static/: 사용자 정의 CSS 등 정적 리소스

## guachi/ 하위 구조
- __init__.py: guachi 모듈 초기화 파일
- config.py: 설정 관리 기능 구현
- database.py: 설정 데이터베이스 기능 구현
- tests/: 단위 및 통합 테스트 코드
  - test_configmapper.py, test_configurations.py, test_database.py, test_integration.py: 각종 테스트 스크립트

## guachi.egg-info/ 하위 구조
- PKG-INFO, SOURCES.txt, dependency_links.txt, top_level.txt: 패키징 및 의존성 정보

---

이 구조는 레거시 프로젝트의 모든 기능과 문서, 테스트, 패키징 정보를 포함하며, 업그레이드 작업 시 각 파일을 최신 Python 및 패키징 표준에 맞게 리팩토링하는 데 활용됩니다.