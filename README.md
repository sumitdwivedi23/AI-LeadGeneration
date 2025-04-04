
---
title: LanggraphAgenticAI
emoji: 🐨
colorFrom: blue
colorTo: red
sdk: streamlit
sdk_version: 1.42.0
app_file: app.py
pinned: false
license: apache-2.0
short_description: Refined langgraphAgenticAIChatbot
---


# 🎯 Lead Generation AI Agent

This application is a **Streamlit-based AI-powered tool** that helps you generate leads by searching for relevant posts and extracting user information from **Quora** and the **web**. The extracted data is formatted and written into a **Google Sheet** for easy access and further analysis.

---

## 🚀 Features

- **AI-Powered Query Transformation**: Converts user queries into concise, focused descriptions using a Groq-based AI model.
- **Search for Leads**:
  - Fetches URLs from **Quora** and the **web** where users are discussing topics related to your query.
- **User Information Extraction**: Extracts detailed user information such as usernames, bios, post types, timestamps, upvotes, and links.
- **Google Sheets Integration**: Automatically writes the extracted data into a new Google Sheet for easy sharing and analysis.

---

## 🛠️ Requirements

### Python Libraries
Install the required libraries using `pip`:
```bash
pip install -r requirements.txt
```

### API Keys
You will need the following API keys:
1. **Firecrawl API Key**: For searching URLs and extracting user information.
2. **GROQ API Key**: For AI-powered query transformation.
3. **Composio API Key**: For Google Sheets integration.

---

## 📂 File Structure

- **`app.py`**: The main application file containing all the logic for lead generation, data extraction, and Google Sheets integration.

---

## ⚙️ How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

4. Open the app in your browser at `http://localhost:8501`.

---

## 📝 Usage

1. **Enter API Keys**:
   - Provide your Firecrawl, GROQ, and Composio API keys in the sidebar.

2. **Describe Your Leads**:
   - Enter a detailed description of the type of leads you're looking for (e.g., "Looking for users who need automated video editing software with AI capabilities").

3. **Generate Leads**:
   - Click the **Generate Leads** button to start the process.

4. **View Results**:
   - The app will:
     - Search for relevant URLs on Quora and the web.
     - Extract user information from the URLs.
     - Write the data into a Google Sheet.
   - A link to the Google Sheet will be displayed if the process is successful.

---

## 📊 Output

The extracted data is written into a Google Sheet with the following columns:
- **Website URL**
- **Username**
- **Bio**
- **Post Type** (Question/Answer)
- **Timestamp**
- **Upvotes**
- **Links**

---

## 🔧 Key Functions

### 1. `search_for_urls`
Fetches URLs from Quora and the web based on the user query.

### 2. `extract_user_info_from_urls`
Extracts detailed user information from the fetched URLs using the Firecrawl API.

### 3. `format_user_info_to_flattened_json`
Formats the extracted user information into a flattened JSON structure for easy processing.

### 4. `create_google_sheets_agent`
Creates a Google Sheets agent using the Composio API for writing data into a new Google Sheet.

### 5. `write_to_google_sheets`
Writes the formatted data into a Google Sheet and returns the link to the sheet.

---

## 🛡️ Error Handling

- **Missing API Keys**: Displays an error if any API key is missing.
- **No URLs Found**: Warns the user if no relevant URLs are found.
- **Google Sheets Error**: Displays an error if the Google Sheet cannot be created.

---

## 🌟 Example

### Input:
- Query: "Looking for users who need automated video editing software with AI capabilities."

### Output:
- A Google Sheet containing user information extracted from Quora and the web.

---

## 🧑‍💻 Contributing

Feel free to submit issues or pull requests to improve the application.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 🙌 Acknowledgments

- **Streamlit**: For building the interactive UI.
- **Firecrawl API**: For web and Quora data extraction.
- **Composio API**: For Google Sheets integration.
- **GROQ AI**: For query transformation.
