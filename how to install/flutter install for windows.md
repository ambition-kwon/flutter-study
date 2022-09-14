# 🤔 Basics of Flutter(for Windows)



## 1. Flutter install

- [flutter homepage](https://docs.flutter.dev/get-started/install/windows) → flutter_windows_3.3.1-stable.zip →  `C:\src` 폴더 생성 후 붙여넣기 →

`시스템환경변수` → 사용자 변수 Path 및 시스템 변수 Path에 `C:\src\flutter\bin` 경로를 각각 새로 등록 → powershell실행 후, `flutter doctor`명령어 입력하여 정상작동 확인 → 2,3,4,5번 진행 → `flutter doctor` 명령어에 대해 모두 초록색 체크박스가 뜬다면 성공 😃

## 2. Git install

- [git homepage](https://git-scm.com/)

## 3. Visual Studio Code install

- [VSC homepage](https://code.visualstudio.com/)

## 4. Android Studio install

- [Android Studio homepage](https://developer.android.com/studio?gclid=EAIaIQobChMI__uPlqmE-gIVFKmWCh1Y6gHLEAAYASAAEgIUg_D_BwE&gclsrc=aw.ds)
- 실행 → Customize → All settings → sdk 검색 → SDK Tools → Android SDK Command-line Tools (latest) check & apply
- 실행 → Customize → All settings → Plugins → Flutter install → Dart install
- powershell 실행 후 아래 명령어 입력(all yes)

```
flutter doctor --android-licenses
```

## 5. Visual Studio install

- [VS homepage](https://visualstudio.microsoft.com/ko/thank-you-downloading-visual-studio/?sku=Professional&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false)→ 수정 → C++을 이용한 데스크톱 개발 install

> 모든 프로그램 설치에 있어 powershell실행 후, `flutter doctor` 명령어를 통해 진행상황을 확인

## 6.  Dart로 “Hello, World!” 출력하기

- 원하는 곳에 새로운 폴더 생성(C:\src\project1) → Android Studio 실행 → Open → 방금 만든 폴더 경로로 지정 → Trust Project → 왼쪽 WorkSpace탭에서 Project1위에 마우스 놓고 오른쪽 클릭 → New → File → test1.dart 입력 → 코드 입력 창 위에 Dart SDK is not configured가 팝업되었을 경우 Open Dart settings → Enable Dart support for the project → Dart SDK path에 `C:\src\flutter\bin\cache\dart-sdk` 등록 → Enable Dart support for the following modules에서 Project1 클릭 후 Apply & OK → 초록색 화살표(실행버튼) 왼쪽 Add Configuration → Add new run configuration → Dart Command line App → Dart file : `C:\src\project1\test1.dart` 선택 후 Apply & OK → 아래 코드 입력 후 Run(초록색 버튼)

```dart
main(){
	print("Hello, World!");
}
```

## 7. Flutter & Dart로 기본 앱 코드(increasing button) 실행시키기

- Android Studio → Projects → 더보기(점 3개) → Virtual Device Manager → Create Device → Pixel 2 → `R`(API level : 30) download → Next → Finish
- Android Studio → New Flutter Project → Flutter → Flutter SDK path : `C:\src\flutter` → 기본 설정으로 Finish → 왼쪽 Workspace에서 lib  / main.dart파일 클릭 → Run Icon(초록색) 왼쪽에 `no device selected` 클릭해서 아까전에 다운받은 Pixel 2로 변경(없다면 Refresh 누르고 새로고침) → Run(최초 실행에 시간 많이 소요됨)

