# PpakAim 설치 및 파일 검증 안내

## 1. 설치 파일 받기

[PpakAim 공식 GitHub Releases](https://github.com/gudtjr980-arch/PpakAim-Download/releases)에서 게시된 설치 파일을 다운로드합니다.

**v1.0.0 배포 완료:** [실제 설치 파일 PpakAim-Setup.exe 다운로드](https://github.com/gudtjr980-arch/PpakAim-Download/releases/download/V1.0.0/PpakAim-Setup.exe)

## 2. 다운로드 파일 SHA-256 확인

게시된 설치 파일 `PpakAim-Setup.exe`의 SHA-256 (GitHub의 파일 메타데이터와 원본 일치 확인):

```text
33e7b2dae8ad60e153cf79bc725771017de128d46901abffe81b9dd50339595a
```

파일 이름만 변경해도 해시는 유지되지만, 파일 본문을 변경하거나 재빌드했다면 새로운 해시를 게시해야 합니다.

Windows PowerShell을 열고 다운로드한 파일 경로에 맞게 실행합니다.

```powershell
Get-FileHash -Algorithm SHA256 "$env:USERPROFILE\Downloads\PpakAim-Setup.exe"
```

출력된 `Hash`가 위 값과 완전히 일치하는지 확인하세요. 일치하지 않으면 실행하지 말고 다운로드한 파일과 배포 공지를 다시 확인하세요.

**참고:** 해시 일치는 배포 원본과의 동일성을 확인할 뿐, 프로그램의 안전성을 보증하지 않습니다.

## 3. 설치

1. 파일을 다운로드한 뒤 위 해시 검사를 수행합니다.
2. 설치 파일을 실행합니다.
3. 설치 화면의 안내에 따라 진행합니다.
4. 실행 후 측정 및 기록 저장이 가능한지 확인합니다.

현재 프로그램은 디지털 코드 서명이 없습니다. Windows에서 '알 수 없는 게시자' 경고가 나타날 수 있습니다. 파일 출처와 무결성을 확인하지 않은 상태에서 경고를 무시하지 마세요. 백신이 악성코드로 탐지한다면 설치를 중단하고 원인을 확인해야 합니다.

## 4. 측정 데이터 백업

개발용 원본 문서상 저장 경로:

```text
%LOCALAPPDATA%\PpakAimDesktop\data\measurements.sqlite3
```

프로그램의 기록 내보내기 기능을 이용하거나, 프로그램을 종료한 후 해당 파일을 별도로 백업하세요. 업데이트 후 기존 기록이 유지되는지는 실제 Windows PC에서 검증 전입니다.

## 5. 오류 제보

[GitHub Issues](https://github.com/gudtjr980-arch/PpakAim-Download/issues)에 Windows 버전, 설치 실패 단계, 오류 메시지를 남겨 주세요. 개인정보는 공개하지 마세요.

## PUBG 및 UGC 훈련장 이용 주의사항

PpakAim은 사격 패턴과 감도 변화를 분석하기 위한 **외부 보조 프로그램**입니다. 게임 메모리 조작, 반동 자동 제어, 마우스 입력 주입 기능은 제공하지 않는 것으로 개발되어 있습니다.

다만 화면 캡처와 마우스 입력 측정 기능을 사용하므로, PUBG 운영 정책이나 안티치트 시스템에 의해 제한 또는 탐지될 가능성을 배제할 수 없습니다.

**PUBG UGC 훈련장에서 사용하더라도 PUBG/KRAFTON의 공식 승인이나 제재 면제를 의미하지 않습니다.** 다른 프로그램의 사용 사례 역시 허용의 근거가 되지 않습니다.

게임 이용약관 및 UGC 모드 규칙을 준수하고, 보안 차단·게임 경고가 나타나면 프로그램 동시 실행을 중단하세요. 보안 기능을 끄거나 탐지를 우회하는 행위는 권장하지 않습니다. 개발자는 게임 계정의 안전을 보증하지 않습니다.
