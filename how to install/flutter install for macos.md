# ๐ค Basics of Flutter(for Mac OS)



## 1. Flutter install

- [flutter homepage](https://docs.flutter.dev/get-started/install/macos) โ flutter_macos_arm64_3.3.1-stable.zip โ  Downloadํด๋์ ์ ์ฅ โ ์๋ ๋ช๋ น์ด ์ฐจ๋ก๋ก ์๋ ฅ โ `flutter doctor` ๋ช๋ น์ด๊ฐ ์ ๋๋ก ์คํ ๋๋ค๋ฉด ์ฑ๊ณต๐

~~~
cd ~
mkdir development
cd /development
unzip ~/Downloads/flutter_macos_arm64_3.3.1-stable.zip
export PATH="$PATH:`pwd`/development/flutter/bin"
~~~

- `flutter doctor`๋ช๋ น์ด ์๋ ฅํ์ฌ ์ ์์๋ ํ์ธ โ 2,3,4,5,6๋ฒ ์งํ โ `flutter doctor` ๋ช๋ น์ด์ ๋ํด ๋ชจ๋ ์ด๋ก์ ์ฒดํฌ๋ฐ์ค๊ฐ ๋ฌ๋ค๋ฉด ์ฑ๊ณต ๐

## 2. XCode install

- Xcode์ค์น๋ฅผ ์ํด ์๋์ ๋ช๋ น์ด ์๋ ฅ

~~~
brew install mas
mas install 497799835
~~~

- install ์๋ฃ ํ, ๋ค์ 2๊ฐ์ ๋ช๋ น์ด ์๋ ฅ(ํญ์ ์ต์  ๋ฒ์ ์ Xcode๋ฅผ ์ ์งํ๋ ๋ช๋ น์ด)

~~~
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
sudo xcodebuild -runFirstLaunch
~~~

- CocoaPods ์ค์น

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
- terminal ์คํ ํ, ์๋ ๋ช๋ น์ด ์๋ ฅ

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

## 7.  Dart๋ก โHello, World!โ ์ถ๋ ฅํ๊ธฐ

- ์ํ๋ ๊ณณ์ ์๋ก์ด ํด๋ ์์ฑ(/Users/์ฌ์ฉ์๋ช/Desktop/project1) -> Android Studio ์คํ โ Open โ ๋ฐฉ๊ธ ๋ง๋  ํด๋ ๊ฒฝ๋ก๋ก ์ง์  โ Trust Project โ ์ผ์ชฝ WorkSpaceํญ์์ Project1์์ ๋ง์ฐ์ค ๋๊ณ  ์ค๋ฅธ์ชฝ ํด๋ฆญ โ New โ File โ test1.dart ์๋ ฅ โ ์ฝ๋ ์๋ ฅ ์ฐฝ ์์ Dart SDK is not configured๊ฐ ํ์๋์์ ๊ฒฝ์ฐ Open Dart settings โ Enable Dart support for the project โ Dart SDK path์ `/Users/์ ์ ๋ช/development/flutter/bin/cache/dart-sdk`๋ฑ๋ก -> Enable Dart support for the following modules์์ Project1 ํด๋ฆญ ํ Apply & OK โ ์ด๋ก์ ํ์ดํ(์คํ๋ฒํผ) ์ผ์ชฝ Add Configuration โ Add new run configuration โ Dart Command line App โ Dart file : `/Users/์ ์ ๋ช/Desktop/project1\test1.dart` ์ ํ ํ Apply & OK โ ์๋ ์ฝ๋ ์๋ ฅ ํ Run(์ด๋ก์ ๋ฒํผ)

~~~dart
main(){
	print("Hello, World!");
}
~~~

## 8. Flutter & Dart๋ก ๊ธฐ๋ณธ ์ฑ ์ฝ๋(increasing button) ์คํ์ํค๊ธฐ

- MAC OS์ ๊ฒฝ์ฐ Virtual Device๊ฐ ๊ธฐ๋ณธ(`Pixel_3a_API_33_arm64-v8a`)์ผ๋ก 1๊ฐ install ๋์ด ์๊ธฐ ๋๋ฌธ์ Create device๋ฅผ ํ๋ ๊ณผ์ ์ ํ์์น ์๋ค. ๋ง์ฝ ์ค์น๋์ด ์์ง ์๋ค๋ฉด ์๋์ ๊ฐ์ ๋ฐฉ๋ฒ์ผ๋ก intallํ๋ฉด ๋๋ค.

    > Android Studio โ Projects โ ๋๋ณด๊ธฐ(์  3๊ฐ) โ Virtual Device Manager โ Create Device โ Pixel 2 โ `R`(API level : 30) download โ Next โ Finish

- Android Studio โ New Flutter Project โ Flutter โ Flutter SDK path : `/Users/์ ์ ๋ช/development/flutter` -> ๊ธฐ๋ณธ ์ค์ ์ผ๋ก Finish โ ์ผ์ชฝ Workspace์์ lib  / main.dartํ์ผ ํด๋ฆญ โ Run Icon(์ด๋ก์) ์ผ์ชฝ์ `no device selected` ํด๋ฆญํด์ ์๊น์ ์ ๋ค์ด๋ฐ์ Pixel 2๋ก ๋ณ๊ฒฝ(์๋ค๋ฉด Refresh ๋๋ฅด๊ณ  ์๋ก๊ณ ์นจ) โ Run(์ต์ด ์คํ์ ์๊ฐ ๋ง์ด ์์๋จ)
