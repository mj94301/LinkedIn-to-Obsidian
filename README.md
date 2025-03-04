LinkedIn Contacts to Markdown for Obsidian

# LinkedIn Contacts to Markdown for Obsidian

This repository provides a Python script to convert your **LinkedIn connections download** into **Markdown files** formatted for use in **Obsidian**. The script structures each connection as an individual Markdown file with YAML frontmatter, enabling easy organization, linking, and visualization in Obsidian's **Graph View**.

## 📌 Overview of the Process

1. **Download Your LinkedIn Connections** from LinkedIn.
2. **Augment the Data in Excel** (Optional) – Add job family categories or any other relevant metadata.
3. **Run the Python Script** – Converts each contact into an individual Markdown file.
4. **Load Files into Obsidian** – Create a tagging and linking structure to enhance Graph View visualization.

---

## 🔹 Step 1: Download Your LinkedIn Contacts

1. Go to **LinkedIn Settings & Privacy** → **Data Privacy** → **Get a copy of your data**.
2. Select **Connections** and request a download.
3. LinkedIn will create a CSV file you can download from that same page (`Connections.csv`).
4. Save the file and **rename it to** `LinkedIn_Connections_Download_YYYYMMDD.csv`.

---

## 🔹 Step 2: Augment Data in Excel (Optional)

- Open the downloaded CSV in Excel or Google Sheets.
- Add custom fields, such as **Job Families** or **Industry Tags**, for better categorization.  (See Excel formula for job families)
- Ensure column names remain unchanged for compatibility with the script.  (Or update the script.)

---

## 🔹 Step 3: Convert Contacts to Markdown

### **Prerequisites**

- Install **Python 3.x** if not already installed.
- Install Pandas:
  ```sh
  pip install pandas
  ```

### **Run the Script**

1. Clone this repository or download the script.
2. Place the `LinkedIn_Connections_Download_YYYYMMDD.csv` file in the same folder as the script.
3. Open a terminal and run:
   ```sh
   python linkedin_to_markdown.py
   ```
4. The script will create a folder called `LinkedIn_Connections_MD` containing individual `.md` files for each contact.

---

## 🔹 Step 4: Load into Obsidian and Create a Labeling Scheme

1. Open **Obsidian** and add `LinkedIn_Connections_MD` to your vault.
2. Use **Graph View** to visualize connections.
3. Establish an internal linking and tagging system:
   - Link contacts to **Companies**: `[[Company Name]]`
   - Categorize by **Job Family**: `[[Job Family]]`
   - Use **Tags** for filtering (e.g., `#networking`, `#consulting`)
   - Under Settings in Graph View use Groups to differentiate using colors

---

## 🔹 Example Markdown Output

```yaml
---
Company: [[Google]]
LinkedIn Company: Google
Position: Senior Software Engineer
Position Category: [[Engineering]]
Connected on: 2023-05-10
city:
state:
Source: LinkedIn download 20250302
---

[LinkedIn Profile](https://www.linkedin.com/in/example)
```

---
