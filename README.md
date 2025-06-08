# datafun-06-eda
Module 6: Perform Custom EDA

## Dataset is a sampling of passengers on the Titanic
https://github.com/mwaskom/seaborn-data/blob/master/titanic.csv 
![image](https://github.com/user-attachments/assets/3fc2be56-b3a5-4514-8266-86e38204f0f4)

## 1. Virtual Environment Management (Windows PowerShell)

1. **Create a virtual environment**
   ```powershell
   py -m venv .venv
   ```

2. **Activate the virtual environment**
   ```powershell
   .\.venv\Scripts\activate
   ```

3. **Upgrade pip, setuptools, and wheel**
   ```powershell
   py -m pip install --upgrade pip setuptools wheel
   ```

4. **Install required packages**
   ```powershell
   py -m pip install --upgrade -r requirements.txt
   ```

---

## 2. Running Python Scripts

- Activate your `.venv` and ensure all required packages are installed.
- Verify all external packages in your scripts are listed in `requirements.txt`.

**Run Python scripts:**
```powershell
py demo_script.py
py do_stats.py
py draw_chart.py
py greet_user.py
```

---

## 3. Repeatable Workflow Checklist

When resuming work on your project, follow these steps:

1. [Pull latest changes](https://github.com/denisecase/pro-analytics-01/tree/main/03-repeatable-workflow)
2. Activate virtual environment
3. Install dependencies
4. Run Python scripts
5. Modify and test code
6. Add, commit, and push changes to Git

---

## 4. Git Add-Commit-Push CheatSheet

```powershell
git clone https://github.com/youraccount/yourrepo
git add .
git commit -m "custom message"
git push -u origin main
git pull origin main
git push
```

---

## P6 Jupyter Notebooks for EDA

### Steps and Notebook Check

1. **Initial Title, Header, and Imports**  
   *(author, purpose, date.  imports: pyarrow, pandas, jupyterlab, seaborn, matplotlib, and Axes from matplotlib.axes)*
2. **Data Acquisition**  
   *(loaded the Iris dataset for classification and basic data task)*
3. **Initial Data Inspection**
   *(checked the dataset's format, size, and the type of information each column)
4. **Initial Descriptive Statistics**
   (summary statistics for numerical columns)
5. **Initial Data Distribution for Numerical Columns**
   **Initial Data Distribution for Categorical Columns**
   (Sepal length and width appear to have a normal distribution. Petal length and width looks to have some abnormal distribution or missing data)
   The distribution of each species is each at 50 per species.
6. **Initial Data (or Data Preprocessing)**
   (Used pandas to clean and transform data; Added sepal area and petal area columns)
7. **Initial Visualizations**
   (Used matplotlib to show pairplot's.  Added a scatter plot to show two numerical variable.)
8. **Initial Storytelling and Presentation**

- **Clear Structure:** The notebook is organized into logical steps, starting from data loading, inspection, cleaning, transformation, visualization, and ending with insights. This helps guide the reader through the EDA process.
- **Descriptive Markdown:** Each section begins with a markdown cell that describes the purpose of the step, making it easy for readers to follow the analysis.
- **Code Comments:** Python code cells include comments explaining what each line does, which helps both beginners and experienced readers understand the workflow.
- **Visual Aids:** Plots and charts are included to visually communicate the distribution of features and relationships between variables, supporting the narrative with visual evidence.
- **Insights and Interpretation:** After each major analysis step, markdown cells summarize findings and interpret results, connecting the data to potential next steps or business questions.
- **Reproducibility:** The notebook uses standard libraries and loads data in a way that others can easily reproduce the analysis.
- **Storytelling Flow:** The notebook tells a story: it starts with a question (exploring the Iris dataset), investigates the data, cleans and transforms it, visualizes key patterns, and ends with actionable insights.
- **Next Steps:** The notebook is ready for further analysis, such as building classification models, based on the clear separation between species found in the EDA.

> **Tip:** For presentations, consider hiding code cells and focusing on markdown explanations and visualizations to make the story accessible to non-technical audiences.

---

### Notebook Checklist

- [x] Exactly one Markdown title (with a single hash)
- [x] Useful Markdown header cell with author, purpose, and optionally, the date
- [x] Numbered second-level Markdown headings for organization
- [x] Numbered sections with useful content for:
    1. Imports
    2. Load Data
    3. Initial Data Inspection
    4. Initial Descriptive Statistics
    5. Initial Data Distribution for Numerical Columns
    6. Initial Data Transformation and Feature Engineering
    7. Initial Visualizations
    8. Initial Storytelling and Presentation
- [x] Commentary throughout that tells a unique data story
- [x] Unique insights into the dataset
- [x] Code and visuals are working, notebook is fully executed and viewable on GitHub

---
