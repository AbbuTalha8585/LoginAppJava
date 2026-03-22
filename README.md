# LoginApp — Android (Java)

A simple two-screen Android login app built with Java. Users enter a username and password, and on success are taken to a Welcome screen.

---

## Screenshots

| Login Screen | Welcome Screen |
|---|---|
| Dark glassmorphism UI with username & password fields | Centered "Welcome 🎉" text on matching dark background |

---

## Features

- Login form with username and password fields
- Password visibility toggle (👁 eye button)
- "Forgot password?" link
- Hardcoded credential check (`admin` / `1234`)
- Toast messages for success and failure
- Navigates to `WelcomeActivity` on successful login
- Dark purple theme (`#110D2B`) with decorative blob drawables
- Glassmorphism card style for the login form

---

## Project Structure

```
app/src/main/
├── java/com/example/login/
│   ├── MainActivity.java        # Login logic
│   └── WelcomeActivity.java     # Welcome screen
├── res/
│   ├── layout/
│   │   ├── activity_main.xml    # Login screen layout
│   │   └── activity_welcome.xml # Welcome screen layout
│   ├── drawable/
│   │   ├── bg_blob_top.xml
│   │   ├── bg_blob_bottom.xml
│   │   ├── bg_glass_card.xml
│   │   ├── bg_input_field.xml
│   │   ├── bg_login_button.xml
│   │   ├── bg_logo_circle.xml
│   │   ├── bg_welcome_circle_inner.xml
│   │   └── bg_welcome_circle_outer.xml
│   └── values/
│       ├── colors.xml
│       ├── strings.xml
│       └── themes.xml
└── AndroidManifest.xml
```

---

## Requirements

| Tool | Version |
|---|---|
| Android Studio | Hedgehog or later |
| Min SDK | 24 (Android 7.0) |
| Target SDK | 36 |
| Java | 11 |
| Gradle | 9.1.0 |

---

## How to Run

1. Clone or download this repository
2. Open the project in **Android Studio**
3. Let Gradle sync finish
4. Run on an emulator or physical device (API 24+)

---

## Login Credentials

> These are hardcoded for demo purposes only.

| Field | Value |
|---|---|
| Username | `admin` |
| Password | `1234` |

---

## How It Works

### MainActivity.java

- Binds `username`, `password`, and `loginBtn` views
- On button click, checks if input matches `admin` / `1234`
- Shows a `Toast` for success or failure
- Launches `WelcomeActivity` via `Intent`

### WelcomeActivity.java

- Loads `activity_welcome.xml`
- Displays a centered "Welcome 🎉" message

---

## Customisation

- **Change credentials** — edit the `if` condition in `MainActivity.java`
- **Change theme colour** — update `#110D2B` in `activity_main.xml` and `activity_welcome.xml`
- **Add real authentication** — replace the hardcoded check with an API call or database query

---

## Dependencies

```toml
appcompat      = "1.6.1"
material       = "1.10.0"
activity       = "1.8.0"
constraintlayout = "2.1.4"
```

---

## License

This project is for educational / demo purposes. Feel free to use and modify it.
