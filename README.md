<div align="center">

# 🌍 OpenHolidayAPI

**The Modern Public Holiday JSON API & Data Explorer**
<br>
Visualize. Fetch. Integrate.

[![Live Demo](https://img.shields.io/badge/Live-Demo-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://worldholidays.xyz)
[![Report Issue](https://img.shields.io/badge/Report-Issue-red?style=for-the-badge&logo=github)](https://github.com/pareshjoshij/OpenHolidayAPI/issues)
[![Sponsor](https://img.shields.io/badge/Sponsor-Project-pink?style=for-the-badge&logo=github-sponsors)](https://github.com/sponsors/pareshjoshij)

</div>

## ⚡ Overview

**OpenHolidayAPI** is your source for reliable, accessible global calendar data. We provide direct JSON access to public holiday schedules for virtually any region on Earth, backed by a sleek explorer interface.

Whether you are building a scheduling platform, training an AI model, or just need to sync your team's calendar, **WorldHolidays.xyz** serves the raw data you need via static JSON endpoints or standard ICS files.

<div align="center">
  
![Open Holiday API _ WorldHolidays xyz - Google Chrome 08-02-2026 10_19_07 AM (2)](https://github.com/user-attachments/assets/7fd74601-d89c-4527-a3d6-d101f263b535)


</div>


## 🚀 API Reference

Our data is served via predictable, static JSON endpoints. **No authentication is required** for public access.

### 📍 Endpoint Structure

Construct your URL using the following pattern:
  ```GET https://worldholidays.xyz/api/nation/{ISO_CODE}/{LOCALE}/{YEAR}.json```
<div align="center">

  
| Parameter | Description | Example |
| :--- | :--- | :--- |
| **`ISO_CODE`** | 2-letter Country/Region code (ISO 3166-1 alpha-2). | `IN`, `US`, `GB` |
| **`LOCALE`** | The language/locale format. | `en_IN`, `en_US` |
| **`YEAR`** | The 4-digit target year. | `2025` |

</div> 

### 🇮🇳 Example: India (2025)

To fetch the public holiday list for India in English for the year 2025:

**Endpoint:** `https://worldholidays.xyz/api/nation/IN/en_IN/2025.json`

#### cURL
```bash
curl -X GET https://worldholidays.xyz/api/nation/IN/en_IN/2025.json
```

#### JavaScript (Fetch)
```javascript
fetch('https://worldholidays.xyz/api/nation/IN/en_IN/2025.json')
  .then(response => response.json())
  .then(holidays => {
    holidays.forEach(holiday => {
      console.log(`${holiday.date}: ${holiday.name}`);
    });
  })
  .catch(error => console.error('Error:', error));
```

#### Python
```python
import requests

url = "https://worldholidays.xyz/api/nation/IN/en_IN/2025.json"
response = requests.get(url)

if response.status_code == 200:
    holidays = response.json()
    for holiday in holidays:
        print(f"{holiday['date']}: {holiday['name']}")
```

---

## ✨ Features

* **🌐 Direct JSON Access**
  Stop parsing HTML or maintaining manual lists. Our endpoints provide clean, machine-readable JSON data formatted perfectly for application development.

* **👨‍💻 Developer-First Console**
  Not sure which locale code to use? Our Live API Console on the website generates the exact endpoint URL and code snippets for you based on your UI selections.

* **📅 Universal Export (.ICS)**
  Need the data offline or in your personal calendar?
  * **One-Click Export:** Instantly download an `.ics` file.
  * **Full Compatibility:** Works seamlessly with Google Calendar, Outlook, and Apple Calendar.

* **🎨 Cyberpunk Explorer**
  * **Dark Mode Aesthetic:** A visually stunning interface to browse holiday data manually.
  * **Dynamic Search:** Quickly find ISO codes and Locales for over 100+ nations.

---

## 💡 How to Use

1. **Select Region:** Choose your target Country/Region from the dropdown.
2. **Set Locale:** (Optional) Define the language or locale specifics.
3. **Get Data:**
   * **For Apps:** Copy the generated JSON Endpoint from the API Console.
   * **For Personal Use:** Click **Download .ICS** to sync with your calendar.

---

## 🐛 Feedback & Data Requests

While our backend logic is maintained internally, this project thrives on community feedback.

* Missing a Regional Holiday?
* Incorrect Date?
* Feature Suggestion?

Please [Open an Issue](https://github.com/pareshjoshij/OpenHolidayAPI/issues) on this repository. Your reports help keep the API accurate for everyone.

---

## ❤️ Support the Project

This service provides free access to global data. If this API powers your application or saves you development time, please consider sponsoring to help cover server costs.

<div align="center">

[**💖 Sponsor via GitHub**](https://github.com/sponsors/pareshjoshij)

<sub>Designed & Developed by <a href="https://github.com/pareshjoshij">pareshjoshij</a></sub>

</div>
