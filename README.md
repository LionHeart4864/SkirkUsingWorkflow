# SkirkUsingWorkflow

This repository shows how to set up and run a Skirk workflow using GitHub Actions and GitHub Codespaces.

<img width="1110" height="570" alt="image" src="https://github.com/user-attachments/assets/7cb3d1a5-c798-43ae-b542-e94b25d4aea7" />


## Requirements

* A GitHub account
* Access to GitHub Codespaces
* A private GitHub repository for the initial setup
* The Skirk client application

## Phase 1 — Initial Setup in GitHub Codespaces

1. Create or use a **private GitHub repository**.

2. Open the repository in **GitHub Codespaces**.

3. Follow the setup instructions from the following project:

   urlSkirk Repository[https://github.com/ShahabSL/Skirk](https://github.com/ShahabSL/Skirk)

4. After the setup is completed, download the `skirk-kit` folder.

5. Keep the following files from the folder:

   * `client.json`
   * `client.skirk`
   * `exit.json`

---

## Phase 2 — Create the Workflow Repository

1. Create a new **public GitHub repository**.

2. You can use a name such as `SkirkUsingWorkflow`.

3. Open your repository and go to:

   `Settings` → `Secrets and variables` → `Actions`

4. Create the following **Repository Secrets**:

### 1. CLIENT_JSON

* Name: `CLIENT_JSON`
* Value: Copy and paste the contents of `client.json`

### 2. CLIENT_SKIRK

* Name: `CLIENT_SKIRK`
* Value: Copy and paste the contents of `client.skirk`

### 3. EXIT_JSON

* Name: `EXIT_JSON`
* Value: Copy and paste the contents of `exit.json`

---

## Phase 3 — Add the GitHub Actions Workflow

1. In your `SkirkUsingWorkflow` repository, go to:

   `Code` → `Add file` → `Create new file`

2. Create the following file:

```text
.github/workflows/skirk.yml
```

3. Copy the workflow content provided by this project into the file.
4. Commit and save the changes.

---

## Phase 4 — Run the Workflow

1. Open the `Actions` tab in your repository.
2. Select the workflow named `Skirk Proxy`.
3. Click `Run workflow`.

---

## Phase 5 — Use the Generated Client Configuration

1. Download and install the Skirk client application from:

   urlSkirk Releases[https://github.com/ShahabSL/Skirk/releases](https://github.com/ShahabSL/Skirk/releases)

2. Copy the generated Skirk client configuration into the application.

**Note: Disable the workflow whenever you do not need to run it using Skirk**
---

## Credits

Special thanks to entity["people","ShahabSL","Creator of the Skirk project"] for creating the Skirk project.
