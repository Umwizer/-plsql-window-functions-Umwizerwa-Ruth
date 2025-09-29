## **1. Problem Definition**

### **Business Context**

**Company**: Academic Analytics Pro (EdTech SaaS Provider)  
**Department**: Customer Success & Educational Insights  
**Industry**: Educational Technology serving universities across East Africa

### **Data Challenge**

University clients using our platform collect extensive student performance data including exam scores, assignment grades, and course completion metrics. However, their current reporting systems only provide basic aggregate statistics like class averages and total scores. This limitation makes it impossible for academic advisors to identify at-risk students early, track individual student progress trends, or segment students for targeted interventions based on relative performance.

### **Expected Outcome**

This analysis will enable university administrators to:

- Proactively identify students in the bottom 20% for early intervention
- Allocate tutoring resources to specific performance segments
- Track student improvement trends across academic terms
- Make data-driven decisions about curriculum adjustments and teaching methodologies

## **2. Success Criteria**

We will implement **5 measurable analytical goals** using PL/SQL window functions:

1. **Top 5 Performing Students per Course** → `RANK()`

   - Identify academic excellence and benchmark performance
   - Enable scholarship and recognition decisions

2. **Running Cumulative GPA Calculation** → `SUM() OVER()`

   - Track progressive academic performance throughout the semester
   - Monitor student trajectory toward graduation requirements

3. **Term-over-Term Grade Improvement Analysis** → `LAG()/LEAD()`

   - Calculate percentage growth or decline between academic periods
   - Measure effectiveness of academic support programs

4. **Student Performance Quartile Segmentation** → `NTILE(4)`

   - Divide students into four equal performance groups
   - Enable differentiated support strategies for each segment

5. **3-Term Moving Average GPA Trends** → `AVG() OVER()`

   - Smooth out grade volatility to identify consistent patterns
   - Predict long-term academic success probabilities

## 3. Database Schema

1. Login as admin ![[Pasted image 20250929145748.png]]
2. Creating Database![[Pasted image 20250929150046.png]]
3. Login as assignment 1![[Pasted image 20250929150128.png]]
4. Creating Students Table![[Pasted image 20250929150515.png]]
5. Creating Courses table![[Pasted image 20250929150624.png]]
6. Creating Grades table![[Pasted image 20250929150759.png]]
7. Creating indexes for better query performances![[Pasted image 20250929151006.png]]![[Pasted image 20250929151048.png]]
8. Inserting sample students ![[Pasted image 20250929151420.png]]
9. inserting course![[Pasted image 20250929151616.png]]
10. inserting grades![[Pasted image 20250929151717.png]]
11. Verfying that data are inserted ![[Pasted image 20250929151836.png]]
12. Creating sequence for each automation id generationg![[Pasted image 20250929151923.png]] ![[Pasted image 20250929151958.png]] ![[Pasted image 20250929152036.png]]
13.
