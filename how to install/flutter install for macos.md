# 🤔 Basics of Flutter(for Mac OS)



## 1. Flutter install

- [flutter homepage](https://docs.flutter.dev/get-started/install/macos) → flutter_macos_arm64_3.3.1-stable.zip →  Download폴더에 저장 → 아래 명령어 차례로 입력 → `flutter doctor` 명령어가 제대로 실행 된다면 성공😃

~~~
cd ~
mkdir development
cd /development
unzip ~/Downloads/flutter_macos_arm64_3.3.1-stable.zip
export PATH="$PATH:`pwd`/development/flutter/bin"
~~~

- `flutter doctor`명령어 입력하여 정상작동 확인 → 2,3,4,5,6번 진행 → `flutter doctor` 명령어에 대해 모두 초록색 체크박스가 뜬다면 성공 😃

## 2. XCode install

- Xcode설치를 위해 아래의 명령어 입력

~~~
brew install mas
mas install 497799835
~~~

- install 완료 후, 다음 2개의 명령어 입력(항상 최신 버전의 Xcode를 유지하는 명령어)

~~~
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
sudo xcodebuild -runFirstLaunch
~~~

- CocoaPods 설치

~~~
brew install cocoapods
~~~

## 3. Chrome install

~~~
brew install cask
brew install google-chrome
~~~

## 4. Android Studio(Toolchain) install

```
brew install android-studio
```

- Customize - All settings - SDK - SDK tools - `Android SDK Command-line Tools(latest)` check & Apply
- terminal 실행 후, 아래 명령어 입력

~~~
flutter doctor --android-licenses
~~~

## 5. Visual Studio Code install

~~~
brew install visual-studio-code
~~~

## 6. IntelliJ IDEA install

~~~
brew install intellij-idea
~~~

## 7.  Dart로 “Hello, World!” 출력하기

- 원하는 곳에 새로운 폴더 생성(/Users/사용자명/Desktop/project1) -> Android Studio 실행 → Open → 방금 만든 폴더 경로로 지정 → Trust Project → 왼쪽 WorkSpace탭에서 Project1위에 마우스 놓고 오른쪽 클릭 → New → File → test1.dart 입력 → 코드 입력 창 위에 Dart SDK is not configured가 팝업되었을 경우 Open Dart settings → Enable Dart support for the project → Dart SDK path에 `/Users/유저명/development/flutter/bin/cache/dart-sdk`등록 -> Enable Dart support for the following modules에서 Project1 클릭 후 Apply & OK → 초록색 화살표(실행버튼) 왼쪽 Add Configuration → Add new run configuration → Dart Command line App → Dart file : `/Users/유저명/Desktop/project1\test1.dart` 선택 후 Apply & OK → 아래 코드 입력 후 Run(초록색 버튼)

~~~dart
main(){
	print("Hello, World!");
}
~~~

## 8. Flutter & Dart로 기본 앱 코드(increasing button) 실행시키기

- MAC OS의 경우 Virtual Device가 기본(`Pixel_3a_API_33_arm64-v8a`)으로 1개 install 되어 있기 때문에 Create device를 하는 과정은 필요치 않다. 만약 설치되어 있지 않다면 아래와 같은 방법으로 intall하면 된다.

    > Android Studio → Projects → 더보기(점 3개) → Virtual Device Manager → Create Device → Pixel 2 → `R`(API level : 30) download → Next → Finish

- Android Studio → New Flutter Project → Flutter → Flutter SDK path : `/Users/유저명/development/flutter` -> 기본 설정으로 Finish → 왼쪽 Workspace에서 lib  / main.dart파일 클릭 → Run Icon(초록색) 왼쪽에 `no device selected` 클릭해서 아까전에 다운받은 Pixel 2로 변경(없다면 Refresh 누르고 새로고침) → Run(최초 실행에 시간 많이 소요됨)
