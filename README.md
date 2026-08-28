
## 🛠️ Tech Stack & Tools

* **Python (Pandas, Matplotlib, Seaborn)**: Data Cleaning, Missing Values Imputation, Feature Engineering.
* **Power BI Desktop**: Data Modeling, Data Visualization, UI/UX Dashboard Design.
* **DAX (Data Analysis Expressions)**: Custom Measures & Calculated Metrics.
* **Power Query**: Data Transformation & Normalization.

---

## 💡 Key Highlights & Engineering Solutions

### 1. Data Cleaning & Feature Engineering (Python)

* **Unstructured Text Processing**: Extracted binary features (`No Smoking`, `No Pets`, `No Parties`, `Quiet Hours`) from the complex `house_rules` column.
* **Missing Value Handling**: Applied contextual missing value imputation based on variable relationships rather than standard global replacements.
* **Data Sanitization**: Cleaned currency strings (removing `$` and commas) and cast data types appropriately (`price`, `service fee`).

### 2. Data Modeling & Normalization

* **Dimensional Modeling**: Separated unstructured text into a normalized `house_rules_table` linked via `listing_id` to maintain schema efficiency and reduce model load.
* **Star Schema Architecture**: Structured fact and dimension tables for optimized Power BI performance.

### 3. Interactive UX/UI (Power BI)

* **Executive Overview**: High-level KPIs (`Total Listings`, `Avg Price`, `Verified Hosts %`, etc.).
* **Drill-Through Pages**: Granular insights per `neighbourhood_group` and `room_type` without cluttering main executive visuals.

---

## 📊 Dashboard Visuals

| Page | Description |
| --- | --- |
| **Executive Overview** | Summary of overall listings, host verification rates, and top-level KPIs. |


<img width="1316" height="812" alt="Excutive Overview" src="https://github.com/user-attachments/assets/94b70c0f-153d-45e2-88e9-b2736dd706e7" />




| **Reviews & Availability** | Guest review patterns, host activity metrics, and rating distributions. |


<img width="1920" height="1080" alt="Review   Availability" src="https://github.com/user-attachments/assets/5c1fea89-12ec-4fc1-9757-b6595c2b15c1" />



| **House Rules** | House Rules |


<img width="1308" height="737" alt="House rules" src="https://github.com/user-attachments/assets/2035b878-4794-48bd-ae03-ada80dd89d29" />



| **Pricing Analysis** | Price distribution across borough groups, room types, and service fee correlations. |


<img width="1306" height="736" alt="Pricing Analysis" src="https://github.com/user-attachments/assets/0c46b8f4-cf23-4222-9030-c070ae4dc340" />



| **Drill-Through Details** | In-depth breakdown per specific neighborhood and listing rules. |


<img width="1920" height="1080" alt="neighbourhood group details" src="https://github.com/user-attachments/assets/54c80cd8-be2d-4199-8b0a-ada54d472ff2" />



---

## 📐 Key DAX Measures Included

* `Total Listings` = 'DISTINCTCOUNT(airbnb_cleaned[id])'
* `Average Price` = 'AVERAGE(airbnb_cleaned[price])'
* `Instant Bookable %` = `DIVIDE([Instant Bookable Listings],[Total Listings],0)`
* Average Rating⭐ = 'AVERAGE(airbnb_cleaned[review rate number])'


---

## 🚀 How to Run the Project

1. **Python Notebook**: Open `Python/Airbnb_Data_Cleaning.ipynb` in Jupyter Notebook or VS Code to review the cleaning pipeline.
2. **Power BI Report**: Download `PowerBI/Airbnb_Dashboard.pbix` and open it using Power BI Desktop.
3. **Documentation**: Refer to `Documentation/Airbnb_Project_Documentation.pdf` for complete project specifications.
