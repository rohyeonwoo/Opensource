# Opensource

오픈소스개발방법론 수업의 실습과 Git 학습 자료를 모았습니다.
기존 비공개 자료를 포함하므로 이 저장소도 Private으로 유지합니다.

| 폴더 | 내용 | 출처 |
| --- | --- | --- |
| [projects/qt-message](projects/qt-message) | Message/Clear 버튼과 텍스트 창, UI/컨트롤 분리 | opensource / main |
| [projects/qt-window](projects/qt-window) | PyQt 기본 창 | open_Test / master |
| [lessons/github](lessons/github) | GitHub 수업 README와 MIT LICENSE | github / main |
| [lessons/open-test](lessons/open-test) | 초기 Git 실습 README | open_Test / main |

## 실행

Python 3 가상환경에 루트의 requirements.txt를 설치한 뒤 실행할 프로젝트 폴더로 이동합니다.
원본 환경은 Python 3.12와 PyQt5 5.15.11을 사용했습니다.

```sh
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
cd projects/qt-message
python main.py
```

기본 창 예제를 실행하려면 `projects/qt-window`에서 `python main.py`를 실행하세요.
아이콘의 상대 경로를 유지하기 위해 각 프로젝트 폴더에서 실행합니다.

## 원본 보존

원본 세 저장소의 브랜치 네 개와 커밋 이력을 모두 보존했습니다.
`sources/<원본 저장소>/<브랜치>` 태그로 통합 전 파일을 확인할 수 있습니다.
원본의 Linux 가상환경(`bin`, `lib`, `lib64`, `pyvenv.cfg`)과 캐시 파일은
현재 프로젝트 폴더에서 제외하고 원본 태그와 로컬 Git bundle 백업에 그대로 남겼습니다.
필요한 패키지는 새 가상환경에 설치하세요.

라이선스는 원본별 범위를 유지합니다. `lessons/github/LICENSE`를 다른 프로젝트 전체에 적용하지 않습니다.
상세 경로와 보존 목록은 [docs/migration.json](docs/migration.json)을 참고하세요.

이번 통합에서는 원본 파일의 Git blob 일치, 전체 이력 도달 가능 여부, Python 구문을 검증했습니다.
GUI 실행은 검증하지 않았습니다.
