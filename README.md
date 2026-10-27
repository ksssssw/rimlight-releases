# Rimlight 배포 저장소

[Rimlight](https://github.com/ksssssw/rimlight-releases/releases)는 macOS 알림을 화면 가장자리 빛과 스낵바 카드로 보여 주는 메뉴 막대 앱입니다.
이 저장소는 **설치 파일(DMG)과 자동 업데이트 피드(`appcast.xml`)만** 담습니다. 소스 코드는 공개하지 않습니다.

## 설치

1. [최신 릴리스](https://github.com/ksssssw/rimlight-releases/releases/latest)에서 `Rimlight-<버전>.dmg`를 받습니다.
2. DMG를 열고 Rimlight를 **응용 프로그램** 폴더로 드래그한 뒤, 응용 프로그램 폴더에서 실행합니다(DMG 안에서 바로 실행하면 권한과 로그인 항목이 유지되지 않습니다).
3. 첫 실행 안내에 따라 **전체 디스크 접근** 권한을 허용합니다. macOS에는 다른 앱의 알림을 읽는 공개 API가 없어 알림 센터 데이터베이스를 읽기 전용으로 읽습니다. 어떤 데이터도 Mac 밖으로 나가지 않습니다.
4. 알림이 두 번 뜨지 않게 하려면 시스템 설정 › 알림에서 앱별 알림 스타일을 "없음"으로 바꿉니다. 알림은 계속 알림 센터에 쌓입니다.

요구 사항: macOS 26 이상(Apple Silicon·Intel 모두).

앱은 Developer ID로 서명하고 Apple 공증을 거쳤습니다. 받은 파일이 손상되지 않았는지 확인하려면 릴리스 본문의 SHA-256과 비교합니다.

```sh
shasum -a 256 ~/Downloads/Rimlight-<버전>.dmg
```

## 업데이트

1.1.0부터 앱이 하루에 한 번 이 저장소의 `appcast.xml`을 확인하고, 새 버전이 있으면 메뉴 막대와 설정에서 알려 줍니다. 메뉴 막대 › "업데이트 확인…"으로 바로 확인할 수도 있습니다.
1.0.0에는 자동 업데이트가 없으므로 한 번만 DMG를 직접 받아 설치해 주세요.

## 변경 기록

각 버전의 변경 내용은 [Releases](https://github.com/ksssssw/rimlight-releases/releases) 본문에 있습니다.

## 문제 신고

[Issues](https://github.com/ksssssw/rimlight-releases/issues)에 남겨 주세요. macOS 버전, Rimlight 버전(메뉴 막대 › Rimlight 정보), 재현 방법을 적어 주시면 도움이 됩니다.

## 라이선스

Rimlight 바이너리는 © 2026 ksssssw. All rights reserved. 개인 용도로 자유롭게 설치해 쓸 수 있으며, 재배포·수정은 허용하지 않습니다.
앱은 [Sparkle](https://sparkle-project.org)(MIT License)을 포함합니다. 전문은 앱의 "Rimlight 정보" 창에 있습니다.
