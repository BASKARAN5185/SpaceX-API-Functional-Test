# 🚀 SpaceX API Functional Testing (Postman)

This repository contains a comprehensive set of **functional tests for the SpaceX public API**, developed using [Postman](https://www.postman.com/). The goal is to verify the functionality, correctness, and stability of various SpaceX API endpoints through automated test cases.

---

## 📌 Project Objectives

- Validate core SpaceX API endpoints such as **launches**, **rockets**, **capsules**, **payloads**, etc.
- Ensure consistent response **status codes**, **body content**, and **data structure**
- Perform **edge case testing** and **parameter validation**
- Use **Postman scripts** for automated test assertions
- Support execution via **Postman GUI** and **Newman CLI**

---

## 🛠️ Tools & Technologies

| Tool      | Purpose                                 |
|-----------|------------------------------------------|
| Postman   | API testing platform                     |
| Newman    | Command-line runner for Postman tests    |
| JavaScript | Postman test scripting language         |

---

## 📁 Repository Structure

```
📦 SpaceX-API-Postman-Tests
├── 📄 README.md
├── 📂 postman
│   ├── SpaceX_Postman_Collection.json
│   └── SpaceX_Environment.json
```

- **`SpaceX_Postman_Collection.json`**: Contains all the request endpoints and associated test scripts
- **`SpaceX_Environment.json`**: Holds environment-specific variables like base URL
- **`README.md`**: Documentation and execution steps

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/SpaceX-API-Postman-Tests.git
cd SpaceX-API-Postman-Tests
```

### 2. Import into Postman

- Open Postman
- Click **Import** > Upload the `SpaceX_Postman_Collection.json` file
- Import the `SpaceX_Environment.json` under the **Environments** tab

### 3. Run Tests in Postman GUI

- Select the imported environment from the top-right dropdown
- Open the collection
- Click **Run** to open the Collection Runner
- Click **Start Test** to execute all requests

---

## ▶️ Running with Newman (CLI Option)

You can also run the tests using [Newman](https://www.npmjs.com/package/newman), Postman's command-line tool.

### Install Newman (if not already)
```bash
npm install -g newman
```

### Run the Collection
```bash
newman run postman/SpaceX_Postman_Collection.json -e postman/SpaceX_Environment.json
```

### Optional: Generate a Report
```bash
newman run postman/SpaceX_Postman_Collection.json -e postman/SpaceX_Environment.json -r cli,html
```

This will create a detailed HTML report in your working directory.

---

## ✅ Test Coverage

| Endpoint         | Method | Test Cases Included                          |
|------------------|--------|-----------------------------------------------|
| `/launches`      | GET    | Status code, data array, pagination          |
| `/rockets`       | GET    | Name match, active status, response time     |
| `/capsules`      | GET    | Field validation, total count check          |
| `/payloads`      | GET    | ID lookup, type verification                 |
| (more...)        | ...    | Additional endpoints can be added easily     |

---

## 📈 Future Enhancements

- Add negative test cases
- Integrate with CI/CD (GitHub Actions or Jenkins)
- Test data-driven variations using CSV/JSON in Postman
- Visual regression testing with custom Newman reporters

---

## 📬 Feedback & Contributions

Contributions are welcome! If you’d like to improve the test coverage or add new features, feel free to fork the repo and create a pull request.
