npx react-native run-android

- 问题：
SyntaxError: Invalid regular expression: /(.*\\__fixtures__\\.*|node_modules[\\\]react[\\\]dist[\\\].*|
- 解决：
```
npm i metro-config@0.59.0
```



- 问题：
Unable to load script from assets 'index.android.bundle'. Make sure your bundle is packaged cirrectly or you`re running a packager server.
- 解决：
将项目目录上的index.js打包到assets目录下
```
cd ..\项目目录\android\app\src\main
mkdir assets
cd ..\项目目录
npx react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/
```


- 问题：
```
Execution failed for task ':app:validateSigningDebug'.
> Unable to delete file 'D:\Github\RNDemoTS\android\app\build\intermediates\validate_signing_config\debug\out'
```
- 解决：
cd ./android
./gradlew clean