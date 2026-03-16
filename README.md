# Servicenow-Network-Request-Automation

## 📘 Overview
This project automates the intake, processing, and resolution of network-related service requests using ServiceNow. It leverages Import Sets, Transform Maps, and workflow automation to streamline IT operations.

## 🎯 Objectives
- Simplify bulk import of network issues via CSV
- Automatically map and transform data into ServiceNow tables
- Trigger workflows for assignment and resolution
- Provide visibility into request status and asset tracking

## 📁 Dataset Structure
The CSV file used for import includes the following columns:

| Employee Name   | Email Address                | Department | Asset Tag | Issue Description          |
|---------------  |------------------------------|------------|-----------|----------------------------|
| Arjun Sharma    | arjun.sharma89@gmail.com     | IT         | LAP1234   | Laptop not booting         |
| Priya Iyer      | priya.iyer_95@outlook.com    | HR         | MON5678   | Monitor screen flickering  |
| Rohan Deshmukh  | rdeshmukh_projects@yahoo.com | Finance    | PHN4321   | Phone not charging         |
| Ananya Reddy    | ananya.reddy2024@icloud.com  | Support    | PRN8765   | Printer paper jam          |

## 🔧 Implementation Steps

1. **Prepare Dataset**  
   - Create a Google Sheet with sample records  
   - Export as CSV with headers in the first row  

2. **Create Data Source**  
   - Navigate to *System Import Sets > Administration > Data Sources*  
   - Type: File | Format: CSV | Delimiter: Comma | Header Row: Enabled  
   - Attach CSV file  

3. **Load Data into Import Set**  
   - Execute *Load Data* from the Data Source  
   - Verify Import Set Table creation  

4. **Review Import Set Table**  
   - Confirm all fields match CSV headers  
   - Resolve any discrepancies  

5. **Create Transform Map**  
   - Link Import Set Table to target table (e.g., `x_custom_network_request`)  
   - Set Coalesce field for upsert logic  
   - Activate the map  

6. **Map Fields**  
   - Use direct mappings for text fields  
   - Apply GlideScript for transformations (e.g., date formatting)  
   - Validate mappings with test runs  

7. **Run Transform**  
   - Execute transform to populate target table  
   - Confirm successful record creation  

8. **Configure Workflows**  
   - Auto-assign based on department  
   - Send notifications to requesters  
   - Track resolution status  

## 👨‍💻 Author
**Aditya Namdeo**  
Second-year B.Tech student  
Baderia Global Institute Of Engineering and Management





