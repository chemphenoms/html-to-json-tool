# 📄 HTML to JSON Extractor

A robust, browser-based utility that parses exported `.html` files (e.g., from MHTML or structured HTML debug tools) and extracts step-wise reasoning data into clean, structured JSON. This tool is especially useful for analyzing LLM-generated step-by-step reasoning outputs, including human feedback and suggestions.

---

## 🧩 Features

* ✅ Upload `.html` files from LLM supervision or annotation tools
* 🧠 Parses all step cards and final answer sections with accurate tagging
* 🔄 Extracts detailed fields including:

  * `step_number`
  * `status` (`correct`, `incorrect`, `rewrite`, `criticize`)
  * `is_step_regenerated`
  * `type` (`reasoning`, `final_answer`)
  * `step_content`, `status_content`, `human_feedback`
* 🧹 Cleans messy whitespace and encodings
* 📋 One-click **Copy JSON** button
* 💻 100% browser-based – no internet or server connection required
* 🔐 Fully private and secure – runs locally

---

## 🧑‍💻 How to Use

1. Open the `index.html` file in a modern browser (Chrome, Firefox, etc.).
2. Click **“Choose HTML file”** to upload a structured `.html` file.
3. The tool automatically parses and formats all step data.
4. JSON output appears in a clean `pre` block.
5. Click **“Copy JSON”** to save the result to your clipboard.

---

## 📂 Project Structure

```plaintext
index.html      → Self-contained app with HTML, CSS, and JS
README.md       → Documentation and usage instructions
```

---

## 📦 JSON Output Format

Each extracted step is returned as an object with this format:

```json
{
  "step_number": 3,
  "status": "incorrect",
  "is_step_regenerated": true,
  "type": "reasoning",
  "step_content": "This is the revised explanation...",
  "status_content": "The original reasoning was flawed because...",
  "human_feedback": "This step could be improved by..."
}
```

Steps are sorted by number and type (`reasoning` steps first, then `final_answer`).

---

## 🛠 Tech Stack

* HTML5 + CSS3 + Vanilla JavaScript
* Uses `DOMParser` and `querySelector` for DOM traversal
* No dependencies or build tools
* Compatible with all modern browsers

---

## 🔐 Privacy Notice

This tool **does not send or store any data**. All processing is performed in your local browser memory, making it suitable for confidential use cases like AI research review or educational evaluations.

---

## 📜 License

Licensed under the **Apache License 2.0**.
You are free to use, modify, and distribute this tool, provided that you include the original license and copyright.

See [LICENSE](https://www.apache.org/licenses/LICENSE-2.0) for more details.
