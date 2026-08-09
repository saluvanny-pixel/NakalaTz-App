# NakalaTz Android

Complete Android/Kotlin project prepared for GitHub Actions cloud builds.

## Build on GitHub

Push the whole project to a GitHub repository. The workflow at
`.github/workflows/build-apk.yml` automatically builds a debug APK on pushes
to `main`, or manually from Actions > Build NakalaTz APK > Run workflow.

The APK is published as the `NakalaTz-APK` artifact.

## JVM compatibility

Java and Kotlin are both configured for JVM 17 to avoid the
`compileDebugJavaWithJavac (1.8)` vs `compileDebugKotlin (17)` error.

## Verification

The app submits the token value and token type to the verification endpoint
configured in `MainActivity.kt`. The server response determines whether the
token is shown as valid or invalid; the app does not bypass server validation.
