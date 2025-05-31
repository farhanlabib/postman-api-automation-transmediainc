# 🧪 Postman Board & List API Automation

This project demonstrates API automation using Postman for the following flow:

1. **Create a new board**
2. **Create a list under the newly created board**
3. **Delete the list**


---

## Collection Overview

| Request Name     | Method | Description                          |
|------------------|--------|--------------------------------------|
| Create Board     | POST   | Creates a new board                  |
| Create List      | POST   | Creates a list under that board      |
| Delete List      | DELETE | Deletes the previously created list  |

---

## Files Included

| File                                        | Description                                 |
|---------------------------------------------|---------------------------------------------|
| `board-automation.postman_collection.json`  | Postman collection (v2.1 format)            |
| `newman-report.html`                        | Newman-generated HTML report (optional)     |
| `README.md`                                 | Project documentation                       |

---

## How to Use

### 1. Export or Clone This Repo

```bash
git clone https://github.com/farhanlabib/postman-api-automation-transmediainc.git
cd postman-api-automation-transmediainc
```

---

### 2. Install Newman HTML Reporter (if not already)

```bash
npm install -g newman
```
```bash
npm install -g newman-reporter-html
```

---

### 3. Run Collection and Generate Report

```bash
newman run board-automation.postman_collection.json \
  --reporters cli,html \
  --reporter-html-export newman-report.html
```

This will:
- Execute all tests
- Generate a user-friendly report at `newman-report.html`

---

## 🔄 Environment & Variables

The Postman collection uses **collection-level variables**:

| Variable Name | Description                             |
|---------------|-----------------------------------------|
| `baseUrl`     | Base URL (e.g. `http://localhost:3000`) |
| `boardId`     | Auto-set from `Create Board`            |
| `listId`      | Auto-set from `Create List`             |


---

## Features

- Fully automated API flow using chained requests
- Dynamic variables for boardId and listId
- Test scripts include `pm.expect()` assertions
- Graceful handling of `200` and `404` scenarios

---


