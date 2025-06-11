# datafun-06-eda
Module 6: Perform Custom EDA
Branton Dawson

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

<https://nwmissouri.instructure.com/courses/69377/assignments/1099285>

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

### Initial Storytelling and Presentation

1. Passenger Demographics
- **Age Distribution:** Most passengers were young adults, with a concentration in their 20s and 30s.
- **Gender Imbalance:** There were nearly twice as many male passengers as female passengers.
- **Class Structure:** The majority of passengers traveled in third class, reflecting the Titanic’s role as a vessel for immigrants and lower-income travelers.
2. Survival Insights
- **Survival Rate:** More than half of the passengers did not survive, highlighting the tragedy’s scale.
- **Class and Survival:** First-class passengers had a much higher survival rate than those in second or third class, showing the impact of social status.
- **Gender and Survival:** Women had a significantly higher survival rate than men, reflecting the "women and children first" policy.
3. Family and Fare
- **Family Size:** Most passengers traveled alone or with one family member; larger families were less common.
- **Fare Distribution:** Ticket prices varied widely, with first-class fares much higher than those in lower classes.
- **Fare by Embarkation:** Passengers embarking from Cherbourg paid higher fares on average, likely due to a higher proportion of first-class travelers.
4. Embarkation Patterns
- **Port of Embarkation:** Most passengers boarded at Southampton, but survival rates and class distributions varied by port.
5. Visual Storytelling
- **Histograms and Count Plots:** Effectively show the distribution of age, fare, class, and gender.
- **Boxplots and Heatmaps:** Reveal relationships between fare, class, and embarkation port.
- **Stacked Bar Plots:** Clearly illustrate survival differences by class and gender.
- **Pairplots:** Help identify correlations and separations between groups.
6. Data Quality
- **Missing Data:** Notable missing values in age and deck columns, which may affect some analyses.
- **Feature Engineering**: Creating new features like family size and fare per person adds depth to the analysis.

---
