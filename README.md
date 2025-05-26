# ElevateLabs_Task1_Data_Cleaning_Excel

		
Data Cleaning Summary: Medical Appointment No Shows Dataset		
		
Date of Analysis: May 26, 2025 Analyst: Surya Velpula Original Dataset: KaggleV2-May-2016.csv		
		
1. Initial Dataset Overview:		
		
Original Dimensions: 110,528 rows and 14 columns.		
Purpose: The dataset tracks medical appointments, specifically whether patients showed up for their scheduled appointments.		
		
		
2. Data Cleaning Actions Performed:		
		
Column Renaming:		
		
ScheduledDay renamed to scheduled_day		
AppointmentDay renamed to appointment_day		
No-show renamed to no_show		
(Optionally mention if Handcap was renamed to handicap for correct spelling, or any other columns if you applied standard snake_case like PatientId to patient_id.)		
Rationale: Ensured consistent, snake_case naming conventions for improved readability and ease of use in future analysis.		
		
Handling Missing Values & Outliers:		
		
Age Column: Identified and removed 1 row where Age was recorded as -1. This was treated as waste/erroneous data, as a negative age is illogical and would distort analysis.		
General Blanks/Nulls: Performed a comprehensive check across all columns using Excel's filter function. No significant blank or null values (other than the Age outlier) were found that required imputation or removal.		
Rationale: Removed invalid data points to maintain data integrity and prevent skewed analytical results. Confirmed overall data completeness.		
		
Duplicate Records:		
		
After the initial check, 1 duplicate row was identified and successfully removed based on an exact match across all columns.		
Rationale: Ensured each record represents a unique appointment entry, preventing overcounting or biased statistics.		
		
Data Type & Format Standardization:		
		
		
no_show Column: Transformed categorical string values (Yes, No) into numerical binary representations (1, 0).		
Yes (patient did NOT show) converted to 1.		
No (patient DID show) converted to 0.		
Rationale: Converted to a numerical format for easier quantitative analysis and compatibility with statistical functions.		
Gender Column: Standardized gender representations from F to f and M to m.		
Rationale: Ensured consistent casing for categorical values, simplifying filtering and grouping.		
Date Columns (scheduled_day, appointment_day): Converted original date strings (e.g., YYYY-MM-DDTHH:MM:SSZ) to a consistent YYYY-MM-DD (Year, Month, Day) date format.		
Rationale: Ensured all dates are uniformly formatted, enabling accurate time-based analysis and comparisons.		
		
		
3. Final Dataset State:		
		
Cleaned Dimensions: 110,527 rows and 14 columns (Original 110,528 - 1 (Duplicate) = 110,527).		
Readiness: The dataset is now clean, consistent, and ready for further exploratory data analysis, visualization, and potential modeling.		
		
		
4. Tools Used:		
		
Microsoft Excel (Data Filters, Find & Replace, Remove Duplicates, Format Cells).		
