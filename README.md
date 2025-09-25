# 🔄 Auto-Backup n8n Workflows to Gitea

> 💾 Automatically back up all n8n workflows to a Gitea Git repository.  
> ⚡ Detects changes before committing — only updates when needed.  
> 🧠 Smart, clean, and fully automated.  
> 👨‍💻 Built with love by [Yusuf • CaymazStudyo](https://caymazstudyo.com)
gggg
---


---

## ✨ Features

- 📥 Fetches all workflows via `n8n` internal API
- 🧠 Detects if the workflow is new or updated
- 🔒 Encodes data to Base64 and commits to Gitea via API
- 🕒 Runs every 45 minutes via Schedule Trigger
- 💡 Uses `PUT` for updates, `POST` for new entries
- ⚙️ Completely stateless — reads live, writes only when needed
- 📂 Uses structured naming and JSON files for each workflow
sex yusuf eray
---

## 🧰 Technologies Used

| Component      | Role                          |
|----------------|-------------------------------|
| `n8n`          | Workflow Orchestrator         |
| `Gitea`        | Git Repository API            |
| `Python Code`  | Base64 Encoding / JSON Logic  |
| `HTTP Request` | Git Push via REST API         |
| `Schedule`     | Triggers every 45 minutes     |

---

## 🚀 Setup Guide

### 1. 🌍 Configure Global Repo Settings

Edit the `Globals` node in n8n and set:

```json
{
  "repo.url": "https://your-gitea-instance.com",
  "repo.name": "workflows",
  "repo.owner": "your-gitea-username"
}
