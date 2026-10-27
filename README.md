# Sample Application

This is a sample Android application demonstrating a basic Android project structure with the Android Gradle build system.

## Running Tests

This project includes two types of tests that can be run using Gradle:

### Unit Tests

Unit tests are located in `app/src/test/` and run on the local Java Virtual Machine (JVM) without requiring a device or emulator. They are fast and useful for testing business logic.

Run unit tests with:
```bash
./gradlew test
```

Or to run tests for a specific build variant (e.g., debug):
```bash
./gradlew testDebug
```

### Instrumentation Tests (Android Tests)

Instrumentation tests are located in `app/src/androidTest/` and run on an Android device or emulator. These tests have access to the Android framework and are useful for testing UI components and Android-specific functionality.

**Prerequisites:**
- An Android device connected via USB with USB debugging enabled, OR
- An Android emulator running and visible via `adb devices`

Run instrumentation tests with:
```bash
./gradlew connectedAndroidTest
```

This command will:
1. Build the application and test APKs
2. Deploy them to the connected device/emulator
3. Run the instrumentation tests
4. Generate a test report

### Running All Tests

To run both unit tests and instrumentation tests, execute:
```bash
./gradlew test connectedAndroidTest
```

### Test Reports

After running tests, HTML reports are generated in:
- Unit tests: `app/build/reports/tests/`
- Instrumentation tests: `app/build/reports/androidTests/`
