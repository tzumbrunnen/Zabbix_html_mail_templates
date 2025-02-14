# Zabbix HTML Email Template

## 📌 Overview
This is a **modern, responsive, and dark-mode-friendly** HTML email template designed for **Zabbix alert notifications**. It provides a **clean, structured layout** with improved readability, suitable for **mobile and desktop email clients**, including **Outlook**.

## 🎯 Features
✅ **Responsive Design** – Works on all devices (desktop & mobile).  
✅ **Dark Mode Support** – Automatically adjusts colors in dark mode.  
✅ **Clear Visual Indicators** – Uses **icons** to improve readability.  
✅ **Zabbix Data Integration** – Dynamically inserts `{EVENT}` variables.  
✅ **Easy Customization** – Modify colors, layout, and content as needed.  

## 🚀 Usage
To use this template in **Zabbix email notifications**, follow these steps:

1. **Go to Zabbix UI** → **Administration** → **Media Types**.
2. Select **Email** and edit the **Message Templates**.
3. Click **Add Template** and choose **HTML** as the content type.
4. Copy and paste the HTML code from `zabbix_email_template.html`.
5. Save the template and test an email notification.

## 🎨 Customization
The template uses **CSS for styling** and **Zabbix macros** to insert dynamic data. You can modify:

- **Colors** (e.g., change the `.problem` background color).
- **Font styles** (`font-family`, `font-size`, etc.).
- **Table structure** (add/remove rows for more details).
- **Icons** (change or remove emojis for a different look).

## 📜 Template Structure
### 🔹 **Header Section**
- Defines **meta tags** for responsive behavior.
- Includes **dark mode support** using CSS media queries.

### 🔹 **Container Section**
- Main wrapper with **rounded corners** and a **shadow effect**.
- Uses **three alert types**:
  - **🟥 `.problem` (Red) for Active Alerts**
  - **🟩 `.resolved` (Green) for Resolved Alerts**
  - **🟦 `.info` (Blue) for General Events**

### 🔹 **Host Information Table**
| Emoji | Field | Description |
|--------|-------|-------------|
| 🏢 | `{HOST.NAME}` | Displays the affected host name. |
| 💻 | `{HOST.CONN}` | Shows the host's IP address. |
| 📝 | `{HOST.DESCRIPTION}` | Provides a brief description of the host. |
| 🌐 | `{PROXY.NAME}` | Displays the Zabbix proxy handling this host. |

### 🔹 **Event Details Table**
| Emoji | Field | Description |
|--------|-------|-------------|
| 🚨 | `{EVENT.NAME}` | Shows the event name with a clickable link. |
| ⚠️ | `{EVENT.SEVERITY}` | Displays the severity level of the issue. |
| 🔎 | `{EVENT.OPDATA}` | Provides additional **operational data**. |
| ⏳ | `{EVENT.TIME} on {EVENT.DATE}` | Displays the event start time. |
| 📊 | `{ITEM.VALUE}` | Shows the latest value of the monitored item. |
| 🆔 | `{EVENT.ID}` | Original event problem ID. |
| ℹ️ | `{EVENT.STATUS}` | Displays the current problem status. |

### 🔹 **Footer Section**
- Displays the monitoring timestamp:  
  ⏰ `"DMD2 Monitoring - {TIME}.fmttime(%Y-%m-%d %H:%M:%S)"`  

## 🖥️ Dark Mode Support
The template **automatically adapts to dark mode**:
- Backgrounds lighten up for better readability (`#2e2e2e → #3a3a3a`).
- Text and links adjust for better contrast.
- Uses **CSS `prefers-color-scheme: dark`** media queries.

## 🔧 Example Output
| Light Mode | Dark Mode |
|------------|------------|
| ![Light Mode Preview](https://via.placeholder.com/600x300/FFFFFF/333333?text=Light+Mode) | ![Dark Mode Preview](https://via.placeholder.com/600x300/2e2e2e/e0e0e0?text=Dark+Mode) |

## 📬 Testing
To test the template:
1. **Go to Zabbix UI** → **Configuration** → **Actions**.
2. Create a test trigger with `{TRIGGER.SEVERITY}`.
3. Assign an email recipient.
4. Trigger an alert and verify email appearance.

## 📌 Notes
- Ensure **Zabbix is configured** to send HTML emails.
- Icons may render differently across email clients (Outlook, Gmail, etc.).
- Test in both **light mode and dark mode**.

## 🛠️ License
This template is open-source and free to use. Modify as needed for your environment.

---
### 🚀 Happy Monitoring with Zabbix!