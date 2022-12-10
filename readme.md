# Flutter Build Actions
Automate your Flutter build process with GitHub Actions.

## Usage
1. Create a new workflow file in your repository at `.github/workflows/flutter-build.yml`
2. Copy flutter-build.yml script from this repository into your workflow file
3. Commit and push your workflow file to your repository
4. To start a build, go to the Actions tab in your repository and click the "Flutter Build" workflow
5. Click the "Run workflow" button and enter the branch name you want to build

## Actions Workflow
The workflow will run the following steps:
1. Checkout the repository
2. Setup SDK 12
3. Initialize Project Version
4. Install Flutter SDK
5. Build APK & AAB
6. Upload APK & AAB as Github Release (will run simultaneously)

The process will take about 10 minutes to complete. Once the build is complete, you can download the APK's and AAB files from the release page.

If you want to automate build flutter after push to github, simply change 'workflow_dispatch' to 'push' (Line 2) in the flutter-build.yaml file.

