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
1. Login as admin ![](./images/Pasted%20image%2020250929145623.png)
2. Creating Database ![](./images/Pasted%20image%2020250929145748.png)

3. Login as assignment 1 ![](./images/Pasted%20image%2020250929150046.png)
4. Creating Students Table ![](./images/Pasted%20image%2020250929150515.png)
5. Creating Courses table ![](./images/Pasted%20image%2020250929150750.png)
6. Creating Grades table ![](./images/Pasted%20image%2020250929150759.png)
7. Creating indexes for better query  performances ![](./images/Pasted%20image%2020250929151231.png)
8. Inserting sample students  ![](./images/Pasted%20image%2020250929151420.png)
9. inserting course ![](./images/Pasted%20image%2020250929151616.png)
10. inserting grades ![](./images/Pasted%20image%2020250929151717.png)
11. Verfying that data are inserted   ![](./images/Pasted%20image%2020250929151836.png )
12. Creating sequence for each automation id generationg  ![](./images/Pasted%20image%2020250929151958.png) ![](./images/Pasted%20image%2020250929151923.png)
 ![](./images/Pasted%20image%2020250929152036.png)
     ### ER Diagram
      ![](./images/Pasted%20image%2020250929161335.png)

##  4. window function Implementation
### 1 Ranking
   ####  1.1 ROW_NUMBER() - Fixed: Specify table for student_id

![](./images/Pasted%20image%2020250929162034.png)
    
   
   ### 1.2 RANK() - Fixed version
![](./images/Pasted%20image%2020250929164624.png)1.3 Dense Rank
    ![](./images/Pasted%20image%2020250929165042.png)
    
   
### Aggregate Functions
2.1 Running total of scores per student
![](./images/Pasted%20image%2020250929165745.png)
2.2  Class Average Comparison
![](./images/Pasted%20image%2020250929165947.png)
### 3 Navigation Function
![](./images/Pasted%20image%2020250929170305.png)
### 4 distribution Function

![](./images/Pasted%20image%2020250929170514.png)
