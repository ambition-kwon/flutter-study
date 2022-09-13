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

- 





## 8. Flutter & Dart로 기본 앱 코드(increasing button) 실행시키기

- 
