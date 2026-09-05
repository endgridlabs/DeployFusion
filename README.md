<div align="center">

<img src="logo.png" alt="EndGrid DeployFusion" width="120"/>

# EndGrid DeployFusion

**Enterprise Application Packaging & Deployment Automation**

[![Version](https://img.shields.io/badge/version-1.0.1-6366F1?style=flat-square)](https://github.com/endgridlabs/DeployFusion/releases)
[![Platform](https://img.shields.io/badge/platform-Windows-blue?style=flat-square)](https://github.com/endgridlabs/DeployFusion)
[![.NET](https://img.shields.io/badge/.NET-10.0-512BD4?style=flat-square)](https://dotnet.microsoft.com/en-us/download/dotnet/10.0)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

*Package once. Deploy everywhere. No scripts required.*

</div>

---

## What is EndGrid DeployFusion?

EndGrid DeployFusion is a **free, open-source Windows desktop tool** built for SCCM (Microsoft Configuration Manager) and Intune administrators. It automates the entire application packaging and deployment pipeline — from a raw `.exe` or `.msi` installer to a fully deployed, collection-targeted SCCM application or Intune Win32 app — in a single click.

Tasks that previously required 30–60 minutes of manual console work (creating the app, writing PSADT scripts, creating collections, setting up deployments) are completed in under **2 minutes**, with zero scripting knowledge required.

This is DeployFusion's **first public release (v1.0.1)** — the tool has been in active daily use packaging real production applications for months beforehand; this release is the first one built for the community.

---

## ✨ Highlights

- **One-click SCCM & Intune deployment** — from a raw installer to a fully deployed, collection-targeted SCCM Application (or Intune Win32 app) in under 2 minutes. Publish to **SCCM, Intune, or both at once** — the two publishes run in parallel with independent success/failure handling.
- **Custom Package Model** — bundle a primary installer with one or more **add-on installers** into a single SCCM/Intune package (e.g. a console app plus its extension tools), each with its own install/uninstall command and its own detection marker, ANDed together for accurate "Installed" status. Supports installers whose setup needs a whole folder of dependencies (CABs, DLLs, sibling files), not just a single file.
- **AI Packaging Assistant** — suggests deployment name, description, silent install/uninstall switches, and a "silent kill switch" to force-close a running app before install. Bring your own key: Anthropic, any OpenAI-compatible endpoint, or a fully local Ollama model.
- **WinGet catalog built in** — search 90,000+ packages inline across four different panels; DeployFusion downloads the installer, resolves the correct silent switches, and tracks new versions for you automatically.
- **Bulk packaging** — import a CSV (or search WinGet directly) and package dozens of applications in one unattended batch run, with per-row confidence badges and on-demand AI suggestions.
- **SCCM legacy Package model** — create classic Packages/Programs alongside the modern Application model, with full parity in Manage Apps.
- **Staged rollouts (Deploy Rings)** — promote an application through Pilot → Early → Broad → Production collections instead of a single all-at-once deployment.
- **Enterprise or Standalone** — run centrally with a shared SQL Server audit database, role-based access control, and multi-admin approval workflows, or run entirely local with SQLite and zero infrastructure. Switch modes at any time.
- **Interactive Teams approvals** — approval cards in Microsoft Teams carry real Approve/Reject buttons, so an Enterprise approver never has to open the app.
- **Dark theme** — a full dark palette across every screen, toggled instantly in Settings, local to each admin's machine.
- **Audit trail everywhere** — every deploy, delete, rename, migration, and supersedence operation is logged with operator, machine, environment, and outcome; exportable to CSV; retained 365 days.
- **Signed, verifiable installer** — the MSI is Authenticode-signed and RFC 3161 timestamped, with a published SHA-256 for every release.

---

## ✨ Features at a Glance

| Feature | Description |
|---|---|
| 🤖 **AI Packaging Assistant** | Suggests deployment name, description, silent install/uninstall switches, and the silent kill switch — BYOK with Anthropic, OpenAI-compatible, or local Ollama; one-click apply to the form |
| 🚀 **One-Click SCCM Deployment** | Creates the app, PSADT wrapper, deployment types, 3 collections, and 3 deployments automatically |
| 📦 **Intune Win32 Publishing** | Packages `.intunewin`, uploads via MS Graph API, creates Azure AD groups and assignments |
| 🔀 **Publish to SCCM + Intune at Once** | A single "Both" target runs both publishes in parallel, with independent success/failure handling and two separate audit entries |
| 🧩 **Custom Package Model** | Bundle a primary installer with one or more add-on installers into one SCCM/Intune package — each component gets its own install/uninstall command and detection marker; supports folder-source installers with dependencies |
| 🎨 **Auto Icon Fetching** | Fetches high-quality app icons automatically from the web |
| 📋 **PSADT v4 Wrapper Generation** | Generates a production-ready PSADT v4 deployment script from your installer |
| 🗂 **Manage Apps** | Browse, edit, rename, retire, redistribute, and delete SCCM applications from a single view |
| 📦 **SCCM Package Model** | Create and manage classic SCCM Packages/Programs alongside modern Applications |
| 🎯 **Deploy Rings** | Stage a rollout through Pilot → Early → Broad → Production collections instead of one all-at-once deployment |
| 📊 **Health Dashboard** | Live compliance statistics across all deployed SCCM applications |
| 🌗 **Dark Theme** | Full dark palette across every screen, toggled instantly in Settings — local to this machine |
| 🔐 **Flexible Auth Modes** | Interactive (user login) and unattended Intune auth via Entra App Registration — client secret or certificate |
| 🌍 **Multi-Profile** | Switch between DEV, UAT, PROD SCCM environments instantly |
| 🔒 **Encrypted Secrets** | Client secrets are DPAPI-encrypted (Machine or CurrentUser scope, configurable) — safe for shared admin servers |
| 📝 **Audit Logging** | Every operation is logged with operator name, machine, environment, and status — SQLite (Standalone) or SQL Server (Enterprise) |
| 🖱 **Drag & Drop** | Drop an installer file directly onto the window to load it |
| 📋 **Bulk Application Packaging** | Import a CSV and package 10, 50, or 100+ apps in a single batch run |
| 🔍 **WinGet Integration** | Search the 90,000+ package WinGet catalog inline — auto-fills metadata and downloads installers automatically |
| 🔄 **Migration Assistant** | Scan and re-deploy legacy SCCM apps with modern PSADT v4 wrappers |
| 🔗 **Supersedence Manager** | Define and apply supersedence chains between application versions in SCCM |
| 🔔 **Teams Notifications & Interactive Approvals** | Real-time alerts for deployments, versions, and ring promotions — with Approve/Reject buttons directly on the Teams card |
| 🏢 **Enterprise Mode** | Centralized approval workflows, SQL Server audit, and multi-admin coordination |
| 🖥 **Standalone Mode** | Lightweight single-machine mode with no centralized infrastructure required |

---

## 📸 Screenshots

> *Screenshots of the Package App, Custom Package Model, Manage Apps, Dashboard, Deploy Rings, and Settings screens.*

*(Coming soon — see the [wiki](https://github.com/endgridlabs/DeployFusion/wiki) for a full walkthrough.)*

---

## 🚀 Deployment Options

### 🏢 Enterprise Deployment

Designed for large-scale organizational rollouts managed centrally by IT teams.

**Features:**
- Centralized deployment management via SQL Server audit database
- Multi-admin coordination with approval workflows
- Role-based access control (Admin / Operator / Read Only)
- Enterprise-wide software distribution tracking
- Approval gates for bulk operations (2+ applications)
- Global settings sync — all admin workstations share configuration

**SCCM / Intune silent install:**
```powershell
# Standard enterprise install
msiexec /i EndGridDeployFusion.msi /qn /l*v "%TEMP%\DeployFusion.log" `
         ENTERPRISE=1 SQLSERVER=MCSCCM01 SQLDB=EndGrid_DeployFusion

# With Intune Win32 (intunewin wrapping)
msiexec /i EndGridDeployFusion.msi /qn ENTERPRISE=1 SQLSERVER=%SQLSERVER% SQLDB=EndGrid_DeployFusion
```

**Registry detection (Intune):**
```
HKLM\SOFTWARE\EndGrid\DeployFusion  →  EnterpriseMode = "1"
```

### 🖥 Standalone Deployment

Lightweight deployment for individual systems, small teams, and environments without centralized infrastructure.

**Features:**
- Simple installation and configuration — no SQL Server required
- Single-user or small-team model with local audit log (SQLite)
- Ideal for independent administrators and lab environments
- Full SCCM and Intune packaging capability without enterprise overhead

**Standard silent install:**
```powershell
msiexec /i EndGridDeployFusion.msi /qn /l*v "%TEMP%\DeployFusion.log"
```

**File detection (SCCM):**
```
%ProgramFiles%\Deploy Fusion\DeployFusion.exe
```

### 🤫 Silent Installation Support

DeployFusion supports fully unattended installations for automated deployment scenarios.

**MSI public properties:**

| Property | Default | Description |
|---|---|---|
| `ENTERPRISE` | `0` | Set to `1` to enable Enterprise mode at install time |
| `SQLSERVER` | *(empty)* | Pre-configure the SQL Server hostname |
| `SQLDB` | `EndGrid_DeployFusion` | Pre-configure the audit database name |

**Example use cases:**

```powershell
# SCCM Application — Install command
msiexec /i EndGridDeployFusion.msi /qn /l*v "%TEMP%\DF.log" ENTERPRISE=1 SQLSERVER=MCSCCM01

# SCCM Application — Uninstall command
msiexec /x {16802928-854D-4522-8395-8E3926955743} /qn

# Intune Win32 — Install command (wrap with IntuneWinAppUtil first)
msiexec /i EndGridDeployFusion.msi /qn ENTERPRISE=1 SQLSERVER=%SQLSERVER% SQLDB=EndGrid_DeployFusion

# Automated provisioning / remote deployment
msiexec /i \\server\share\EndGridDeployFusion.msi /qn /l*v "%TEMP%\DF.log"
```

---

## 🔧 Prerequisites

Before installing or building DeployFusion, ensure the following are in place:

### On the machine running DeployFusion

| Requirement | Details |
|---|---|
| **Windows 10/11 or Windows Server 2019+** | x64 only |
| **.NET 10.0 Desktop Runtime** | [Download here](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) |
| **SCCM Admin Console** | Must be installed. The tool auto-detects it at `E:\SCCM\AdminConsole\bin`, `C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin`, or `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin` |
| **Network access to SCCM Site Server** | TCP port 135 (RPC) must be open |
| **SCCM Administrator rights** | The account running the tool needs Full Administrator role in SCCM |

### For Enterprise mode (optional)

| Requirement | Details |
|---|---|
| **SQL Server** | Any edition — Express, Standard, or Enterprise |
| **SQL Database** | Created automatically on first launch; default name `EndGrid_DeployFusion` |
| **SQL permissions** | The running account needs `db_owner` on the audit database |

### For Intune publishing (optional)

| Requirement | Details |
|---|---|
| **Microsoft Entra App Registration** | Required for unattended mode (see [Entra Setup](#-entra-app-registration-setup)) — client secret or certificate |
| **Internet connectivity** | Required to reach `graph.microsoft.com` |
| **IntuneWinAppUtil.exe** | Downloaded automatically on first Intune publish |

---

## 🚀 Installation

### Option 1: Install from MSI (Recommended)

1. Download the latest `EndGridDeployFusion-1.0.1.msi` from the [Releases](https://github.com/endgridlabs/DeployFusion/releases) page.
2. Verify the download against the **SHA-256** hash published with the release, and check the digital signature (*Properties → Digital Signatures*).
3. Run the installer. It will install to `C:\Program Files\Deploy Fusion\` by default.
4. Launch **EndGrid DeployFusion** from the Start Menu.

> **Enterprise rollout:** Use the silent install command above with `ENTERPRISE=1` and `SQLSERVER` properties to pre-configure every workstation from SCCM or Intune.

### Option 2: Build from Source

```powershell
# 1. Clone the repository
git clone https://github.com/endgridlabs/DeployFusion.git
cd DeployFusion

# 2. Restore NuGet packages
dotnet restore DeployFusion.csproj

# 3. Build (auto-detects SCCM Admin Console path)
dotnet build DeployFusion.csproj --configuration Release

# 4. Run
.\bin\Release\net10.0-windows\DeployFusion.exe
```

> **Note:** Building requires the SCCM Admin Console to be installed on the build machine, as the SCCM SDK DLLs are referenced from the console's `bin` folder.

### Option 3: Build the MSI Installer

```powershell
# Requires .NET 10 SDK
.\Build-Msi.ps1

# With code signing
.\Build-Msi.ps1 -SignCertThumbprint "YOUR_CERT_THUMBPRINT"

# Output: dist\EndGridDeployFusion.msi
```

---

## ⚙️ First-Time Setup

### 1. Configure Your SCCM Environment

1. Open **Settings** from the left navigation bar.
2. Fill in the following fields:

| Field | Description | Example |
|---|---|---|
| **Profile Name** | A friendly name for this environment | `PROD` |
| **SCCM Server** | Hostname of your SMS Provider / Site Server | `SCCM01.contoso.com` |
| **Site Code** | Your 3-character SCCM site code | `PS1` |
| **Default Shared Drive Path** | UNC path where application source folders are created | `\\sccm01\Sources\Applications` |

3. Click **🔌 Test Connection** to verify connectivity.
4. Click **💾 Save Settings**. The tool validates the SCCM connection before saving.

### 2. Choose Your Deployment Mode

On first launch, the **First-Run Wizard** guides you through selecting your deployment mode:

- **Enterprise** — connects to a SQL Server for centralized audit logging and multi-admin approval workflows
- **Standalone** — uses a local SQLite database; no server infrastructure required

### 3. Configure Intune (Optional)

If you plan to publish applications to Intune:

#### Interactive Login (Simpler)

1. Leave the **"Use Unattended App Registration"** checkbox **unchecked**.
2. When you publish to Intune, a browser window will open for you to sign in with your Microsoft account. Your session is cached for future operations.

#### Unattended / Service Account Mode (Recommended for Servers)

1. Check **"Use Unattended App Registration (Client Secret instead of Interactive Login)"**.
2. Enter the three credentials from your Entra App Registration:

| Field | Where to find it |
|---|---|
| **Directory (Tenant) ID** | Entra portal → App registrations → Your app → Overview |
| **Application (Client) ID** | Entra portal → App registrations → Your app → Overview |
| **Client Secret** | Entra portal → App registrations → Your app → Certificates & secrets |

Certificate-based auth is also supported (no secret-expiry churn on service accounts) — set an **Intune Certificate Thumbprint** instead of a client secret.

3. Click **Save Settings**. The secret is encrypted using **DPAPI**, scoped to **Machine** (default for existing installs) or **CurrentUser** (default for fresh installs, and always available as a toggle in Settings) — it cannot be decrypted on another machine, or by another Windows account under CurrentUser scope.

---

## 🔐 Entra App Registration Setup

To use unattended Intune publishing, create an App Registration in Microsoft Entra:

1. Sign in to [https://entra.microsoft.com](https://entra.microsoft.com)
2. Navigate to **App registrations** → **New registration**
3. Give it a name (e.g., `DeployFusion-Automation`) and click **Register**
4. Note the **Directory (tenant) ID** and **Application (client) ID** from the Overview page
5. Go to **Certificates & secrets** → **New client secret** → Set expiry → **Add**
6. Copy the secret **value** immediately (it won't be shown again)
7. Go to **API permissions** → **Add a permission** → **Microsoft Graph** → **Application permissions**
8. Add the following permissions:

| Permission | Purpose |
|---|---|
| `DeviceManagementApps.ReadWrite.All` | Create and manage Win32 apps in Intune |
| `Group.ReadWrite.All` | Create and manage Azure AD security groups |

9. Click **Grant admin consent**

---

## 📦 Packaging & Deploying an Application

### SCCM Deployment

1. Click **📦 Package App** in the left navigation bar.
2. Click **Browse** (or drag and drop your installer file onto the window).
3. The tool automatically pre-fills:
   - Application name (from the file name)
   - Publisher / Manufacturer (from file metadata)
   - Install arguments (from the MSI product database or common patterns)
   - Application icon (fetched automatically from the web)
4. Review and adjust the fields if needed.
5. Choose your deployment options:
   - **Destination Path** — overrides the profile default if needed
   - **Distribute to All DPs** — tick to trigger content distribution immediately
   - **Target Platform** — SCCM, Intune, or **Both** (parallel publish to both platforms)
   - **SCCM Model** — modern Application model (recommended) or classic Package/Program model
6. Click **🚀 Build & Publish**.
7. Review the confirmation dialog, then click **Deploy**.

**What happens automatically:**

```
Step 1 ── Prepare file system
         └─ Creates \\server\share\AppName\
         └─ Copies installer to Files\
         └─ Generates PSADT v4 wrapper (Invoke-AppDeployToolkit.ps1)
         └─ Fetches and places application icon in SupportFiles\

Step 2 ── Create SCCM Application
         └─ Creates SMS_Application via WMI/SDK
         └─ Adds Script Deployment Type with registry detection
         └─ Sets application icon

Step 3 ── Distribute content (optional)
         └─ Sends to "All Distribution Points" group

Step 4 ── Create 3 Device Collections (in SoftwareDistribution folder)
         └─ AppName - Required
         └─ AppName - Uninstall
         └─ AppName - Available

Step 5 ── Create 3 Deployments
         └─ Required install → Required collection
         └─ Required uninstall → Uninstall collection
         └─ Available install → Available collection
```

### Intune Deployment

When the **Intune** (or **Both**) target is selected:

```
Step 1 ── Download IntuneWinAppUtil.exe (first time only, from Microsoft GitHub)
Step 2 ── Wrap installer + PSADT in .intunewin package
Step 3 ── Authenticate (interactive browser, app secret, or certificate)
Step 4 ── Create Win32 app in Intune via MS Graph API
Step 5 ── Upload encrypted package via Azure Blob Block protocol
Step 6 ── Create 3 Azure AD Security Groups (Available, Required, Uninstall)
Step 7 ── Assign groups to the Intune app
```

---

## 🧩 Custom Package Model

Some real-world installs aren't a single file — a console app that ships with an extension tool, or a setup that needs its whole folder of dependencies (CABs, DLLs, sibling files) rather than just the one `.exe`. The **Custom Package** tab handles both:

1. Click **📚 Custom Package** in the left navigation bar.
2. Set the **Primary Application** — a single file, or a whole setup **folder** with an entry-point file inside it.
3. Add one or more **Add-Ons** — each with its own installer (file or folder), install/uninstall arguments, and optional MSI transform. Known apps (e.g. the SCCM Console + Right Click Tools) auto-fill high-confidence install arguments, including the active profile's site server where relevant.
4. Click **🔍 Inspect MSI Properties…** on any MSI-based component to read its real Property table before guessing at silent-install properties.
5. Choose the target platform (SCCM / Intune / Both) and, for SCCM, the Application or legacy Package model.
6. Click **Build & Publish**.

**What gets built:** one PSADT wrapper that installs the primary, then each add-on in order (an add-on that fails to install is logged and skipped — it never blocks the rest of the package). Uninstall runs in reverse order, add-ons first. Each component gets its own registry detection marker, and SCCM/Intune detection **ANDs across every component** — the app only reports "Installed" once everything it's supposed to contain is actually present.

Renaming or updating a Custom Package Model app in Manage Apps carries its add-on set forward correctly — the add-ons are re-staged and re-detected along with the primary, not silently dropped.

---

## 📋 Bulk Application Packaging

The Bulk Import panel lets you package dozens of applications in a single unattended batch run.

1. Click **📋 Bulk Import** in the left navigation bar.
2. Click **Browse CSV** and select a CSV file with one app per row (or add rows via **🔍 Add from WinGet** — see below).

**CSV format:**

```csv
AppName,Manufacturer,Description,InstallerPath,InstallArguments,UninstallArguments
7-Zip 23.01,Igor Pavlov,File archiver,\\server\sources\7z2301-x64.msi,/qn,/qn
Google Chrome 120,Google,Web browser,\\server\sources\ChromeSetup.exe,/silent /install,
```

3. Review the imported list. Rows that need attention (a silent switch couldn't be resolved) are flagged immediately with a color-coded confidence badge — open the row and use **🤖 AI Suggest** for an on-demand suggestion, reviewed before it's applied.
4. Use **✕ Remove Selected** to exclude individual rows, or **🗑 Clear All** to start over.
5. Choose the target platform (SCCM / Intune / Both) and click **🚀 Run Batch**. Each application is packaged and deployed sequentially; "Both" batches show per-target status columns and a **Partial** state if only one side succeeds.

> **Approval note:** Batches of 2 or more applications in Enterprise mode with approval enabled will be queued for approval before execution.

---

## 🔍 WinGet Integration

DeployFusion integrates with the Windows Package Manager (WinGet) catalog across four panels, letting you search, package, and monitor apps without ever manually downloading an installer.

### Package App — Inline Catalog Search

A **Winget Lookup** bar sits at the top of the Package App panel. Type any application name and DeployFusion queries the WinGet catalog in real time:

- Results show the **Package ID**, latest version, and publisher
- Selecting a result auto-fills the app name, publisher, version, and silent install/uninstall arguments — using the same confidence-based precedence as Bulk Import (known apps use DeployFusion's maintained switches, otherwise the WinGet manifest, then AI)
- When you drop a local installer file onto the window, DeployFusion automatically triggers a WinGet search using the detected app name

### Bulk Import — No Local Installer Required

Click **🔍 Add from WinGet** in the Bulk Import panel to search the catalog and add packages directly to the batch queue. Entries added this way are marked as **WinGet-only**:

- No local `.exe` or `.msi` file needed
- DeployFusion downloads the installer automatically at build time using `winget download`
- Install/uninstall switches follow a confidence-based precedence (identical in Package App and Bulk Import):
  - **Known application (high confidence)** → always DeployFusion's maintained switches, overriding the WinGet manifest
  - **Medium confidence** → the WinGet manifest switches
  - **Low confidence** (unknown app, no usable manifest switch) → an AI-generated suggestion when an AI provider is configured
- The batch grid shows a `✅ Package.ID` badge on matched rows and `⚪ Not matched` on unmatched ones

**Mixed batches are fully supported** — some rows can use local files, others can be WinGet-only.

### Manage Apps — Version Monitoring

Assign a **WinGet Package ID** to any deployed SCCM or Intune application from the details sidebar. Once mapped, DeployFusion checks the WinGet catalog for newer versions:

- **On-demand:** Click **Check Winget Versions** in the toolbar
- **Scheduled:** Enable _WinGet version monitoring_ in Settings with a configurable interval (days). Checks run automatically in the background and send a Teams alert when an update is found
- **Auto-update:** trigger a one-click update straight from a detected new version — the superseding SCCM app (or updated Intune content version) is built and published for you

WinGet mappings are persisted in the audit database so they survive app restarts.

### Supersedence Manager — Fetch via WinGet

When defining a supersedence relationship, use **⬇ Fetch via WinGet** to download the latest installer and auto-populate all fields for the superseding application, without manually sourcing the new installer.

---

## 🔄 Migration Assistant

The Migration Assistant scans your existing SCCM environment and re-deploys legacy applications using modern DeployFusion standards.

1. Click **🔄 Migration** in the left navigation bar.
2. Click **Scan SCCM Apps** to load your existing SCCM application catalog.
3. Select the applications you want to migrate.
4. Click **Migrate Selected** — DeployFusion will:
   - Generate a fresh PSADT v4 wrapper for each selected app
   - Apply the standardized dual-registry detection method
   - Create new collections and deployments under the DeployFusion naming convention

> **Note:** The original SCCM application is left untouched. Migration creates new applications alongside the originals.

---

## 🔗 Supersedence Manager

The Supersedence Manager lets you define upgrade relationships between application versions without using the SCCM console.

1. Click **🔗 Supersedence** in the left navigation bar.
2. Select a **Superseded** (old) application from the list.
3. Select the **Superseding** (new) application.
4. Choose the supersedence behavior:
   - **Upgrade** — install the new version alongside (or replacing) the old
   - **Uninstall** — uninstall the old version before installing the new one
5. Click **Apply Supersedence**. The relationship is written directly to SCCM via the SDK.

---

## 🎯 Deploy Rings

Stage a rollout instead of pushing to everyone at once.

1. Click **🎯 Deploy Rings** in the left navigation bar.
2. Select an application and choose the ring template — the 4-ring standard (Pilot 5% → Early 20% → Broad 70% → Production 100%) or a custom split.
3. Click **Create Ring Collections** — DeployFusion creates one device collection plus a Required deployment per ring in SCCM.
4. Promote to the next ring once you're satisfied with the current one's compliance; ring promotions can post a Teams notification so the whole team has visibility into rollout progress.

---

## 🗂 Managing Applications

Click **Manage Apps** to browse all SCCM applications (and **Intune Apps** for Win32 apps).

| Action | Description |
|---|---|
| **Refresh Apps** | Reload the application list from SCCM / Intune |
| **Export CSV** | Export the list to a CSV file |
| **Select an app** | Opens a details sidebar with full metadata, detection methods, and collection info |
| **Edit Details** | Update Description, Publisher, and Version directly from the sidebar |
| **Rename** | Renames the app, all collections, all deployments, and the source folder atomically — Custom Package Model add-ons are carried forward correctly |
| **⏸ Retire / ▶️ Restore** | Retire (disable) or restore an application |
| **Redistribute** | Re-trigger content distribution to all DPs |
| **⬆️ Update** | Push a new installer as a new content version (Intune) or a superseding app (SCCM) — assignments/detection are kept and renamed to the new version |
| **🗑 Delete** | Removes deployments, content, collections, the application, and the source folder |

> **Approval note (Enterprise mode):** Deleting 2 or more applications simultaneously is queued for approval. Single-application deletions execute immediately.

---

## 🔔 Teams Notifications & Approvals

DeployFusion posts real-time cards to Microsoft Teams (or any compatible incoming webhook endpoint) so your team stays informed without checking the app — and Enterprise approvers can act **directly from the card**, with real Approve/Reject buttons (see `TEAMS_APPROVAL_SETUP.md`).

### Setup

In **Settings → Notifications**, configure one or more webhook URLs:

| Setting | Event |
|---|---|
| **General webhook** (`NotificationWebhookUrl`) | Catch-all — fires for all event types if specific URLs are not set |
| **Deployments** (`WebhookUrlDeployments`) | SCCM / Intune deployment results and ring promotions |
| **Version Alerts** (`WebhookUrlVersionAlerts`) | WinGet version update detected for a deployed app |
| **Approvals** (`WebhookUrlApprovals`) | Approval requests and rejection results (Enterprise mode) |

Specific URLs take precedence over the general webhook. You can route each event type to a different Teams channel.

### Notification Types

#### ✔ Deployment Results
Posted after every SCCM or Intune packaging operation — success or failure. Includes app name, target system (SCCM / Intune), operator, environment profile, and error detail on failure.

#### 🔔 Approval Requests
When a bulk operation (2+ apps) is queued for approval in Enterprise mode, a card is posted immediately with **Approve / Reject buttons** so approvers can act without opening DeployFusion.

#### ✕ Rejection Notifications
If an approver rejects a queued operation, a rejection card is posted with the app name, operation type, and the name of the rejecting admin.

#### ⬆ Version Update Alerts
Triggered when WinGet reports a newer version of a deployed application (via scheduled monitoring or on-demand check). Includes the app name, currently deployed version, and the latest available version.

#### 💫 Ring Promotions
Posted when an application is promoted from one deployment ring to the next (e.g., Pilot → Early → Broad → Production), giving the whole team visibility into rollout progress.

---

## 📊 Health Dashboard

The Dashboard shows a real-time compliance summary across all deployed applications, sourced live from SCCM:

- **Total Success** — devices with the app installed successfully
- **In Progress** — devices with a pending or in-progress deployment
- **Total Errors** — devices with a failed deployment

The data grid shows per-collection compliance percentages with an inline progress bar.

---

## 🏗 Architecture & Technical Details

### Technology Stack

| Layer | Technology |
|---|---|
| UI Framework | WPF (.NET 10.0-windows) |
| SCCM Connectivity | WMI / WqlConnectionManager (native SCCM SDK) |
| SCCM Application Model | `Microsoft.ConfigurationManagement.ApplicationManagement` SDK |
| Intune API | Microsoft Graph REST API (`/beta/deviceAppManagement`) |
| Authentication | MSAL.NET (`Microsoft.Identity.Client`) |
| Secret Encryption | `System.Security.Cryptography.ProtectedData` (DPAPI, Machine or CurrentUser scope) |
| Audit Logging (Standalone) | SQLite via `Microsoft.Data.Sqlite` |
| Audit Logging (Enterprise) | SQL Server via `Microsoft.Data.SqlClient` |
| PSADT Packaging | PSAppDeployToolkit v4 (embedded as `PSADT.zip`) |
| Intune Packaging | IntuneWinAppUtil.exe (auto-downloaded from Microsoft) |
| WinGet Bootstrap | Microsoft's official winget-cli MSIX bundle + VCLibs/WindowsAppRuntime, fetched from the latest [microsoft/winget-cli](https://github.com/microsoft/winget-cli) release and bundled in the installer so machines without WinGet get it silently on first launch — see `Build-Msi.ps1` §1 |
| Icon Fetching | `IconFetcher.cs` — multi-source web fetching |
| Settings | JSON file at `%ProgramData%\EndGrid\DeployFusion\appsettings_v2.json` |
| MSI Installer | WiX v5 SDK |

Full third-party credits (licenses, what's bundled vs. what's a build-time NuGet
reference) are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

### Configuration File

Settings are stored at:
```
C:\ProgramData\EndGrid\DeployFusion\appsettings_v2.json
```

The installer sets `BUILTIN\Users` read/write permissions on this directory so all admin accounts can persist settings without requiring elevation.

### Audit Log

Every deployment, deletion, rename, migration, and supersedence operation is persisted to the audit database:

- **Standalone:** `%ProgramData%\EndGrid\DeployFusion\Logs\AuditLog.db` (SQLite)
- **Enterprise:** SQL Server table in `EndGrid_DeployFusion` database

| Column | Type | Description |
|---|---|---|
| `Id` | INTEGER | Auto-incremented primary key |
| `Timestamp` | TEXT | UTC timestamp (ISO 8601) |
| `OperationType` | TEXT | `DEPLOY`, `DELETE`, `RENAME`, `RETIRE`, `MIGRATE`, `SUPERSEDE`, etc. |
| `AppName` | TEXT | Application name |
| `Operator` | TEXT | Windows username |
| `Machine` | TEXT | Machine hostname |
| `Environment` | TEXT | Active environment profile (DEV / UAT / PROD) |
| `Status` | TEXT | `SUCCESS`, `FAILED`, `PENDING`, `APPROVED`, `REJECTED` |
| `Details` | TEXT | Error message or success summary |

Entries older than **365 days** are automatically purged on startup (PENDING entries are preserved indefinitely).

## 🔒 Data & Privacy

DeployFusion is an on-premises desktop tool — there is no EndGrid-operated backend it
reports to. Everything below stays inside your own environment.

- **Audit log fields.** As documented above, `Operator` (Windows username) and
  `Machine` (hostname) are personal data under GDPR and similar regimes — they identify
  the IT admin who performed an action. They're stored only in the local SQLite file
  (Standalone) or your own SQL Server (Enterprise), retained 365 days, then auto-purged.
  There's currently no built-in "erase this one operator's history" tool beyond the
  age-based purge — if you need per-subject deletion for compliance, query the audit
  table directly (`AuditDatabase.cs` / `SqlServerAuditRepository.cs`).
- **Enterprise mode (SQL Server) makes you the data controller.** Centralizing audit
  and approval records in a SQL Server you host and manage means your organization —
  not EndGrid Labs — is the GDPR data controller for that data, the same as with any
  other internally-hosted admin tool.
- **AI packaging assistant is opt-in and BYOK.** It's off until you configure your own
  Anthropic, OpenAI-compatible, or local Ollama key in Settings. When enabled against a
  cloud provider, prompts can include application/publisher names and install paths —
  never audit-log identifiers (operator, machine name). A local Ollama endpoint keeps
  this data on your own network entirely. Review this before enabling a cloud provider
  in a regulated environment.
- **Secrets** (Intune client secret, AI API key) are DPAPI-encrypted locally, scoped to
  Machine or CurrentUser per your Settings toggle, and never synced to the shared SQL
  DB — see [SECURITY.md](SECURITY.md) for the full secret-storage model.
- **The landing page** ([deployfusion.in](https://deployfusion.in)) sets no cookies and
  runs no analytics — see its [Privacy Policy](https://deployfusion.in/privacy.html)
  (also in `LandingPage/privacy.html`).

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes and ensure the project builds: `dotnet build`
4. **Commit** with a descriptive message: `git commit -m "Add: description of change"`
5. **Push** to your fork: `git push origin feature/your-feature-name`
6. Open a **Pull Request** against `main`

### Building Requirements for Contributors

- Visual Studio 2022 or JetBrains Rider
- .NET 10 SDK
- SCCM Admin Console installed locally (for SDK DLL resolution)

### Running the Test Suite

The test project is multi-targeted so the cross-platform subset runs without a Windows
machine or the SCCM SDK:

```powershell
# Full suite (Windows only, incl. WPF converter tests)
dotnet test DeployFusion.Tests/DeployFusion.Tests.csproj

# Cross-platform subset (works on macOS/Linux and in CI)
dotnet test DeployFusion.Tests/DeployFusion.Tests.csproj -f net10.0
```

### Project Structure

```
DeployFusion/
├── MainWindow.xaml              # Main UI — all panels
├── MainWindow.xaml.cs           # UI code-behind and event handlers
├── MainWindow.BulkImport.cs     # Bulk packaging panel logic
├── MainWindow.MultiPackage.cs   # Custom Package Model panel logic
├── MainWindow.Migration.cs      # Migration assistant panel logic
├── MainWindow.Supersedence.cs   # Supersedence manager panel logic
├── SCCMAutomation.cs            # All SCCM operations (WMI/SDK)
├── IntuneAutomation.cs          # Intune pipeline (package, upload, assign)
├── PSADTBuilder.cs              # PSADT v4 wrapper generation
├── BulkPackagingManager.cs      # Batch packaging orchestration
├── MigrationAssistant.cs        # Legacy app migration logic
├── SupersedenceManager.cs       # Supersedence chain management
├── AddOnComponentResolver.cs    # Custom Package Model add-on persistence/resolution
├── ConfigManager.cs             # Settings load/save/encrypt
├── AuditDatabase.cs             # SQLite / SQL Server audit log
├── ThemeManager.cs              # Light/Dark theme switching
├── IconFetcher.cs               # Web-based icon retrieval
├── App.xaml                     # WPF application entry point
├── App.xaml.cs                  # App startup and global exception handling
├── Directory.Build.props        # Single version source for app + MSI
├── PSADT.zip                    # Embedded PSADT v4 template
├── logo.png                     # Application logo
├── App.ico                      # Application icon (32-bit ARGB, multi-size)
├── DeployFusion.Tests/          # xUnit test project (multi-targeted)
├── LandingPage/                 # Product landing page source
│   ├── index.html
│   ├── style.css
│   ├── app.js
│   └── logo.png
└── Setup/
    ├── Setup.wixproj            # WiX v5 SDK project
    ├── Product.wxs              # MSI installer definition
    ├── Components.wxs           # Auto-harvested publish output
    └── Generate-Assets.ps1      # Installer bitmap/icon generation
```

---

## 🐛 Troubleshooting

### "Cannot find ConfigurationManager.psd1"

The SCCM Admin Console must be installed on the machine. The tool checks these paths:
- `E:\SCCM\AdminConsole\bin`
- `C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin`
- `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin`

If your console is installed elsewhere, build with:
```powershell
dotnet build /p:AdminConsoleBinPath="D:\YourPath\AdminConsole\bin"
```

### "Connection timed out on port 135"

Ensure the SCCM Site Server is reachable from the machine running DeployFusion on **TCP port 135 (RPC)**. This is required for the WMI/WQL connection.

### "Intune App Secret Key is missing"

The **"Use Unattended App Registration"** checkbox is enabled but no secret was saved. Go to Settings, expand the Entra fields, enter the Client Secret, and click **Save Settings**.

### "IntuneWinAppUtil exited with code 1"

Ensure the installer file path does not contain special characters. The file is copied to a temp directory first, so very long paths can also cause issues on Windows.

### Settings not saved after restart

If `C:\ProgramData\EndGrid\DeployFusion` has a restrictive ACL (e.g., created by SYSTEM during a previous install), the app logs a warning but continues operating with in-memory settings. **Re-run the latest MSI installer** — it sets `BUILTIN\Users` read/write on the directory, permanently fixing the permissions.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for full text. DeployFusion embeds and bundles a
few third-party components (PSAppDeployToolkit, winget-cli, and others) under their own
licenses — see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for the full list and
credits.

```
Copyright (c) 2026 EndGrid Labs

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is provided
to do so, subject to the following conditions:
...
```

---

## 👤 Author

**Navaneethkrishnan Malaiyappan**  
EndGrid Labs — [https://deployfusion.in](https://deployfusion.in)  
Personal — [https://navaneethmalaiyappan.com](https://navaneethmalaiyappan.com)

---

<div align="center">

*Built with ❤️ for IT administrators who deserve better tools.*

⭐ **Star this repo** if DeployFusion saves you time!

</div>
