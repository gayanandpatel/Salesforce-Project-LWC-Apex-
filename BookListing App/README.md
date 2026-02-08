# 📚 Book Listing App (LWC)

A modern, responsive Book Search Application built on the Salesforce Platform using **Lightning Web Components (LWC)**. This application allows users to search for books, view details like ratings and publication dates, and browse results in a clean grid layout.

## 📸 Screenshots

| **Search Interface** | **App Launcher Integration** |
|:---:|:---:|
| ![Book Listing App UI](https://github.com/gayanandpatel/Salesforce-Project-LWC-Apex-/raw/main/BookListing%20App/booklisting_app.gif) | ![App Launcher](https://github.com/gayanandpatel/Salesforce-Project-LWC-Apex-/raw/main/BookListing%20App/booklisting_homepage.gif) |
| *Real-time book search with dynamic card rendering and metadata display.* | *Accessible directly from the Salesforce App Launcher.* |

## ✨ Features

-   **Search Functionality:** A robust search bar that queries book data based on user input (titles, keywords).
-   **Dynamic Results Grid:** Displays search results in a responsive grid layout using individual cards for each book.
-   **Rich Metadata Display:** Each book card showcases key details including:
    -   Book Cover / Thumbnail
    -   Full Title
    -   Published Date
    -   Average Rating (handling 'NA' scenarios gracefully)
-   **Interactive UI:** Includes quality-of-life features like a "Clear Search" button (x) to quickly reset the input field.
-   **Responsive Design:** Optimized for various screen sizes using the **Salesforce Lightning Design System (SLDS)**.
-   **App Page Integration:** Deployed as a standalone Lightning App Page, accessible via the App Launcher.

## 🛠️ Tech Stack

-   **Frontend:** Lightning Web Components (LWC), HTML, CSS, JavaScript.
-   **Backend:** Apex (likely used for HTTP Callouts to an external Books API, e.g., Google Books, or complex SOQL queries).
-   **Styling:** Salesforce Lightning Design System (SLDS).
-   **Tools:** VS Code, Salesforce CLI (SFDX), Git.

## 🚀 Installation & Usage

### Prerequisites
-   Salesforce DX project set up.
-   VS Code with Salesforce Extension Pack.
-   Authorized Dev Hub or Scratch Org.

### Deployment Steps

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/gayanandpatel/Salesforce-Project-LWC-Apex-.git](https://github.com/gayanandpatel/Salesforce-Project-LWC-Apex-.git)
    cd Salesforce-Project-LWC-Apex-
    ```

2.  **Authorize your Org:**
    ```bash
    sfdx auth:web:login -d -a myDevOrg
    ```

3.  **Deploy Source to Org:**
    Right-click on the `BookListing App` folder in VS Code and select **SFDX: Deploy Source to Org**.
    *Or run via CLI:*
    ```bash
    sfdx force:source:deploy -p "BookListing App" -u myDevOrg
    ```

4.  **Remote Site Settings (If applicable):**
    If this app uses an external API (like Google Books), ensure you add the API endpoint to the **Remote Site Settings** in Salesforce Setup.

5.  **Add to Page:**
    -   Go to **Setup > Lightning App Builder**.
    -   Edit an existing App Page or create a new one.
    -   Drag and drop the `BookListing` component onto the canvas.
    -   Save and Activate.

6.  **Access the App:**
    Open the **App Launcher** (9 dots), search for **"BookListing App"**, and launch the application.

## 📂 Project Structure

```text
BookListing App/
├── classes/               # Apex Controllers (API Callouts/Logic)
├── lwc/
│   ├── bookListing/       # Main Container Component
│   │   ├── bookListing.html
│   │   ├── bookListing.js
│   │   └── bookListing.css
│   ├── bookTile/          # (Optional) Child component for individual cards
└── tabs/                  # Custom Tab definition
```
---  

## 👤 Author
**Gayanand Patel**