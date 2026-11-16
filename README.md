# Qishen Creator Workbench

中文界面名称：自媒体工作台。

A desktop Obsidian workspace with bundled blank report templates, database views, styles, and optional vault preferences.

## Install

Copy `main.js`, `manifest.json`, and `styles.css` into your vault's `.obsidian/plugins/workspace-preset-kit/` folder. Restart Obsidian and enable **Qishen Creator Workbench** in Community plugins. First test in an empty vault.

In the plugin settings, choose **安装资源** to add missing templates and views. Choose **应用配置** separately to import editor preferences, appearance, template and daily-note paths, hotkeys, graph defaults, and core-plugin switches. Restart Obsidian afterward. Existing resource files are preserved unless you explicitly enable overwrite. Changing the configuration folder uses the vault's configured location for the installer; some inherited workspace features still assume `.obsidian`.

## Included

- A personal workbench with work and personal categories, structured records and report editing.
- 38 blank resources: report templates, template documentation, database views, module configuration and a style snippet.
- Seven optional settings groups, including the bundled module's keyboard shortcuts.
- Journaled import and restore. Restore skips files changed after import.

Global settings affect the entire vault. Configuration changes are opt-in. Installation does not synchronize devices. Install the package on each desktop and use a separate vault synchronization service for personal content.

## Privacy and external services

The release contains generic source code, blank templates and sanitized preferences. It excludes private notes, business records, original attachments, drafts, backups, workspace history, calendar identifiers, credentials and local account configuration. The plugin has no bundled API keys or signed-in session. Normal editing is local. Optional AI features send the selected context to the provider you configure; optional video metadata retrieval contacts the source platform. Review the context before using these features.

External system-calendar integration has been removed. Calendar entries are local vault records; editing or deleting a previously imported entry does not modify its original system-calendar event. The external script-assistant launcher has been removed; manual script editing remains available. This release remains desktop-only because report rendering still uses Node.js crypto and desktop external-link handling; mobile compatibility has not been verified. No guarantee of community-directory acceptance is made.

## File access and optional connections

Backups use only Obsidian vault APIs and are written to `工作台备份/` inside the vault. Daily backups are deduplicated; manual backups use separate folders. The backup folder is excluded from its own source set. A completion marker is written only after all copies succeed. Existing external backups are left untouched. Vault-local backups share the vault storage and synchronization fate, so keep a separate external backup for recovery from total vault loss.

Optional AI writing uses DeepSeek, Alibaba Cloud Qwen, OpenAI, or the compatible API endpoint you configure. These services may require an account and paid API usage. Video metadata lookup uses YouTube or Bilibili. Opening selected external links contacts their destination; downloading a referenced PDF or image contacts its source. These actions depend on the relevant network service and are not required to install the blank templates.

## Recovery

Use **恢复上次导入** to restore the last import. Recovery journals remain inside the plugin's `profile-backups` folder and may contain your pre-import settings: they are local runtime data and must never be included in a public release. Removing the plugin does not remove installed templates or settings. Use restore before uninstalling when needed.

## Verification

JavaScript syntax and bundle loading were checked. In-memory adapter tests cover preserving existing templates, settings merge, restore, repeated installation, edited-file protection, explicit overwrite and rollback after a simulated write failure. A real Obsidian UI installation has not yet been tested.

## Screenshots / 界面预览

### 首页与模块导航

![自媒体工作台首页与模块导航](./screenshot-home.png)

### 创意内容库

![创意内容库卡片与筛选](./screenshot-content.png)

Screenshots show an existing configured workspace. Displayed records are not bundled with the plugin.

## 2.6.4

Removed native calendar bridge and process execution. Backups now stay inside the vault. No Node.js filesystem access remains in the release. The plugin still scans vault records and may show other review recommendations.

## 2.6.5

Opening the cooperation archive in a fresh vault initializes an empty HTML archive and linked record from the bundled template. Existing archives are preserved. The archive location follows the current workspace root.
