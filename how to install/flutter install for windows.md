# π€ Basics of Flutter(for Windows)



## 1. Flutter install

- [flutter homepage](https://docs.flutter.dev/get-started/install/windows) β flutter_windows_3.3.1-stable.zip β  `C:\src` ν΄λ μμ± ν λΆμ¬λ£κΈ° β

`μμ€ννκ²½λ³μ` β μ¬μ©μ λ³μ Path λ° μμ€ν λ³μ Pathμ `C:\src\flutter\bin` κ²½λ‘λ₯Ό κ°κ° μλ‘ λ±λ‘ β powershellμ€ν ν, `flutter doctor`λͺλ Ήμ΄ μλ ₯νμ¬ μ μμλ νμΈ β 2,3,4,5λ² μ§ν β `flutter doctor` λͺλ Ήμ΄μ λν΄ λͺ¨λ μ΄λ‘μ μ²΄ν¬λ°μ€κ° λ¬λ€λ©΄ μ±κ³΅ π

## 2. Git install

- [git homepage](https://git-scm.com/)

## 3. Visual Studio Code install

- [VSC homepage](https://code.visualstudio.com/)

## 4. Android Studio install

- [Android Studio homepage](https://developer.android.com/studio?gclid=EAIaIQobChMI__uPlqmE-gIVFKmWCh1Y6gHLEAAYASAAEgIUg_D_BwE&gclsrc=aw.ds)
- μ€ν β Customize β All settings β sdk κ²μ β SDK Tools β Android SDK Command-line Tools (latest) check & apply
- μ€ν β Customize β All settings β Plugins β Flutter install β Dart install
- powershell μ€ν ν μλ λͺλ Ήμ΄ μλ ₯(all yes)

```
flutter doctor --android-licenses
```

## 5. Visual Studio install

- [VS homepage](https://visualstudio.microsoft.com/ko/thank-you-downloading-visual-studio/?sku=Professional&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false)β μμ  β C++μ μ΄μ©ν λ°μ€ν¬ν± κ°λ° install

> λͺ¨λ  νλ‘κ·Έλ¨ μ€μΉμ μμ΄ powershellμ€ν ν, `flutter doctor` λͺλ Ήμ΄λ₯Ό ν΅ν΄ μ§νμν©μ νμΈ

## 6.  Dartλ‘ βHello, World!β μΆλ ₯νκΈ°

- μνλ κ³³μ μλ‘μ΄ ν΄λ μμ±(C:\src\project1) β Android Studio μ€ν β Open β λ°©κΈ λ§λ  ν΄λ κ²½λ‘λ‘ μ§μ  β Trust Project β μΌμͺ½ WorkSpaceν­μμ Project1μμ λ§μ°μ€ λκ³  μ€λ₯Έμͺ½ ν΄λ¦­ β New β File β test1.dart μλ ₯ β μ½λ μλ ₯ μ°½ μμ Dart SDK is not configuredκ° νμλμμ κ²½μ° Open Dart settings β Enable Dart support for the project β Dart SDK pathμ `C:\src\flutter\bin\cache\dart-sdk` λ±λ‘ β Enable Dart support for the following modulesμμ Project1 ν΄λ¦­ ν Apply & OK β μ΄λ‘μ νμ΄ν(μ€νλ²νΌ) μΌμͺ½ Add Configuration β Add new run configuration β Dart Command line App β Dart file : `C:\src\project1\test1.dart` μ ν ν Apply & OK β μλ μ½λ μλ ₯ ν Run(μ΄λ‘μ λ²νΌ)

```dart
main(){
	print("Hello, World!");
}
```

## 7. Flutter & Dartλ‘ κΈ°λ³Έ μ± μ½λ(increasing button) μ€νμν€κΈ°

- Android Studio β Projects β λλ³΄κΈ°(μ  3κ°) β Virtual Device Manager β Create Device β Pixel 2 β `R`(API level : 30) download β Next β Finish
- Android Studio β New Flutter Project β Flutter β Flutter SDK path : `C:\src\flutter` β κΈ°λ³Έ μ€μ μΌλ‘ Finish β μΌμͺ½ Workspaceμμ lib  / main.dartνμΌ ν΄λ¦­ β Run Icon(μ΄λ‘μ) μΌμͺ½μ `no device selected` ν΄λ¦­ν΄μ μκΉμ μ λ€μ΄λ°μ Pixel 2λ‘ λ³κ²½(μλ€λ©΄ Refresh λλ₯΄κ³  μλ‘κ³ μΉ¨) β Run(μ΅μ΄ μ€νμ μκ° λ§μ΄ μμλ¨)

