# 📊 Meal Tracker Excel Project

A simple **Excel-based Meal Tracker** to help you track your daily **Lunch and Dinner consumption**, calculate total cost automatically, and visualize your eating habits clearly.

---

## ✅ Features

- Auto-generated **Date and Day** columns  
- Dropdowns or manual entry for **Yes/No** in Lunch and Dinner  
- Conditional formatting:  
    - Green highlight for "Yes"  
    - Red highlight for "No"  
- Automatic calculation of **daily total cost** (₹100 per day if both Lunch & Dinner are Yes)  
- Monthly summary of:  
    - Total Lunch consumed  
    - Total Dinner consumed  
    - Total Amount to be Paid  

---

## 💡 How to Use

1. Mark **"Yes"** or **"No"** in the Lunch and Dinner columns for each day.  
2. The **Total column** will calculate the cost automatically:  
   - ₹50 for each Yes in Lunch and ₹50 for each Yes in Dinner.  
3. At the bottom of the table, see:  
   - Total number of Lunch and Dinner consumed.  
   - Final total cost for the month.

---

## ⚡ Formulas Used

- **Date Increment (A3):**  
  ```excel
  =A2 + 1

   Day Name (B2):

  =TEXT(A2, "dddd")


  Daily Total Cost (E2):

  =IF(C2="Yes",50,0) + IF(D2="Yes",50,0)


  Monthly Lunch Count (C33):

  =COUNTIF(C2:C31, "Yes")


  Monthly Dinner Count (D33):

  =COUNTIF(D2:D31, "Yes")


  Monthly Total Amount (E33):

  =(COUNTIF(C2:C31, "Yes") + COUNTIF(D2:D31, "Yes")) * 50





