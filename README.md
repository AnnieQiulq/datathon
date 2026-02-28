# Datathon

_ _

---

## 1.Overview



---

## 2.Features

### 2.1. 


---

### 2.2. 






---

### 2.3. 

---

### 2.4. 

---

## 3.Architecture


---

## 4.Tech Stack

- **Language:** Java (JDK 21)
- **UI:** JavaFX (FXML + controllers)
- **Build:** Maven (multi-module: `core`, `app-fx`)
- **Testing:** JUnit
- **HTTP client:** `java.net.http.HttpClient`
- **Database:** SQL-based storage for users (local); in-memory storage for events
- **Architecture:** Clean Architecture / hexagonal style

---

## 5.Project Structure

```text
SmartCalendar/
├─ core/
│  ├─ src/main/java/
│  │  ├─ entity/
│  │  ├─ use_case/
│  │  ├─ data_access/
│  │  └─ interface_adapter/
│  └─ pom.xml
├─ app-fx/
│  ├─ src/main/java/com/smartcalendar/fx/
│  │  ├─ App.java
│  │  └─ MainController.java (and other controllers)
│  ├─ src/main/resources/com/smartcalendar/fx/
│  │  ├─ MainView.fxml
│  │  ├─ LoginView.fxml
│  │  ├─ SignupView.fxml
│  │  └─ style.css
│  └─ pom.xml
├─ pom.xml          # Parent POM (aggregates modules)
└─ README.md
```

---

## 6.Build & Run

### Prerequisites

- **JDK 21** installed.
- Maven installed or integrated in your IDE (IntelliJ IDEA recommended).
- JavaFX available via the **javafx-maven-plugin** (configured in `app-fx/pom.xml`).

### Clone

```bash
git clone https://github.com/JacobChan182/SmartCalendar.git
cd SmartCalendar
```

### Build

From the project root:

```bash
mvn clean install -DskipTests
```

This builds both `core` and `app-fx`.

### Run (Maven)

From the project root:

```bash
mvn -pl app-fx -am javafx:run
```

- `-pl app-fx` – run only the JavaFX module.
- `-am` – build dependencies (e.g. `core`) automatically.

### Run (IDE)

- Import the project as a **Maven project**.
- Set the run configuration to:
    - Module: `app-fx`
    - Main class: `com.smartcalendar.fx.App`
- Run.

---

## 7.Usage

1. **L**
    - 
    - 
    - 

---

## 8.Roadmap

- [x] Multi-module Maven project (`core`, `app-fx`)
- [x] Login & signup UI integrated with core
- [x] Monthly calendar grid with event pills and `+n` overflow
- [x] Event creation via double-click dialog
- [x] Event editing via dialog
- [x] Event deletion workflow
- [x] Color suggestions with ColorPicker + external API
- [x] Weather assistant for user-typed city/country
- [x] Persistent event storage (JSON/SQLite)
- [x] General UX polish and bug fixing

---

## 9.Contribution Guidelines

- Use feature branches (e.g. `feat/edit-event-ui`, `feat/weather-panel`).
- Keep commits focused and descriptive (e.g., `feat: add edit event dialog`).
- Run `mvn test` before opening a pull request.
- For UI changes, include a short description and, if possible, a screenshot.

---

## 10.License

**All rights reserved. No license granted.**

