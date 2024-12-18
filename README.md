# 파노라마 생성 애플리케이션

이 애플리케이션은 웹캠으로 촬영한 여러 영상 프레임을 기반으로 파노라마를 생성하는 데 목적을 둔 데스크톱 애플리케이션입니다. OpenCV와 PyQt5를 활용해 강력한 영상 처리와 직관적인 GUI를 제공합니다.

---

## **개발 목적**
1. **파노라마 제작 경험 제공**:
   - 영상 처리 기술을 쉽게 체험할 수 있도록 함.
   - 카메라 프레임을 활용해 이미지 처리와 알고리즘 작동 원리를 이해하는 데 기여.
2. **사용자 친화적 인터페이스**:
   - 직관적인 GUI를 통해 기술적 지식이 없는 사용자도 쉽게 활용 가능.
3. **학습과 응용의 기회**:
   - OpenCV의 Stitching API 및 PyQt5의 GUI 설계를 학습.
   - 영상 수집, 봉합, 저장과 같은 작업의 전체 흐름을 이해.

---

## **구체적 구현 내용**
1. **영상 수집**:
   - 웹캠을 통해 프레임을 실시간으로 수집하며 `c` 키로 저장, `q` 키로 종료.
2. **프레임 보기**:
   - 수집된 프레임을 축소하여 연결된 형태로 미리보기 제공.
3. **파노라마 봉합**:
   - OpenCV의 `Stitcher_create` 기능으로 파노라마를 생성.
   - 성공 여부를 GUI 및 알림음으로 표시.
4. **결과 저장**:
   - PyQt5의 `QFileDialog`를 사용해 사용자 지정 경로에 파노라마 저장.
5. **종료**:
   - 리소스를 안전하게 해제하며 애플리케이션 종료.

---

## **개발 환경**
- **운영체제**: Windows 10
- **Python 버전**: 3.11.3
- **IDE**: PyCharm 또는 VS Code
- **필요한 라이브러리**:
  - PyQt5==5.15.11
  - opencv-python==4.10.0.84
  - numpy==1.23.5

---

## **설치 및 실행 방법**
1. **Python 환경 설정**:
   - Python 3.11.3 버전을 설치합니다.
   - 설치할 경로에 가상환경을 생성합니다.:
     ```bash
     python -m venv 가상환경이름
     ```
   - 가상환경을 활성화합니다.:
     ```
     source 가상환경이름/Scripts/activate
     ```
   - 다음 명령어로 필요한 라이브러리를 설치합니다:
     ```bash
     pip install PyQt5 opencv-python numpy
     ```

2. **애플리케이션 실행**:
   - 소스 코드를 `main.py` 파일로 저장합니다.
   - 터미널에서 다음 명령어를 실행하여 애플리케이션을 시작합니다:
     ```bash
     python main.py
     ```

3. **사용 방법**:
   - `영상 수집` 버튼을 눌러 웹캠 영상을 확인하며 `c` 키로 프레임을 캡처하고 `q` 키로 종료합니다.
   - `영상 보기` 버튼으로 캡처한 이미지를 확인합니다.
   - `봉합` 버튼으로 파노라마를 생성합니다.
   - `저장` 버튼으로 결과물을 저장합니다.
   - `나가기` 버튼으로 프로그램을 종료합니다.

---

4. **실행 파일 패키징**:
   - Python이 설치되지 않은 환경에서도 실행하려면 PyInstaller를 사용하여 실행 파일을 생성할 수 있습니다:
     ```bash
     pip install pyinstaller
     pyinstaller --onefile --noconsole main.py
     ```
   - 생성된 실행 파일은 `main.exe`에서 확인할 수 있습니다.

---