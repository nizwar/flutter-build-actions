# Flutter Build Actions
Automate your Flutter build process with GitHub Actions.

Simply run this command in your project root directory to add the workflow file:
`git clone https://github.com/nizwar/flutter-build-actions.git .github/workflows && rm -rf .github/workflows/.git`

or Follow the steps below to add the workflow file manually.
## Usage
1. Create a new workflow file in your repository at `.github/workflows/flutter-build.yml`
2. Copy flutter-build.yml script from this repository into your workflow file
3. Commit and push your workflow file to your repository
4. It will start building your project automatically when you push a commit remotely

# Actions Workflow
The workflow will run the following steps:
1. Checkout the repository
2. Setup SDK 12
3. Initialize Project Version
4. Install Flutter SDK
5. Build APK & AAB
6. Upload APK & AAB as Github Release (will run simultaneously)

The process will take about 10 minutes to complete. Once the build is complete, you will receive an email and you can download the APK's and AAB files from the release page.

If you want to manually trigger the workflow, simply change "push" to "workflow_dispatch" (LINE 2), and then trigger it by clicking the "Run workflow" button in the Actions tab.
