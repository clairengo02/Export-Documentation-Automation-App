# Export-Documentation-Automation-App
Business analysis and Figma prototype project for automating export document preparation and reducing manual data entry.

## Project Overview

The project was developed to address inefficiencies caused by frequent manual updates to export documents, including packing lists, commercial invoices and Vietnamese customs stamps for Trany Australia company

The proposed solution is a mobile application that uses predefined templates, drop-down fields, input validation and document export functionality to reduce manual typing and minimise errors.

## Business Problem

The existing process relied heavily on manual document preparation, creating risks such as:

- Repetitive data entry
- Typographical errors
- Inconsistent document formatting
- Time-consuming updates
- Difficulty reusing previously entered information

## Project Objective

The objective was to design a solution that:

- Automates frequently used field values
- Provides predefined document templates
- Validates user input
- Allows documents to be exported as PDF or Word
- Stores recent documents for later review
- Supports both English and Vietnamese interfaces

## Project Scope

The project scope was defined to clarify the key features, deliverables, stakeholders, and limitations of the proposed export document automation app.

![Project Scope Statement](Project%20Scope%20Statement.png)

## User Stories

1. As a manager, I want a pre-defined drop-down list for certain applicable mandatory fields such as product name, company name, destination, customer name…etc. so that I can simply click and add values without typing. 

2. As a business analyst, I want to have an input validation so that if I enter an incorrect format, a warning message appears and prevents me from proceeding to save or export the document.

3. As a manager, I want to export completed export documents in PDF and Word formats so that I can save, review, and submit them easily.

4. As a manager, I want those completed export documents to be stored so that I can review or edit later if necessary. 

5. As a manager, I want a mobile app to prepare export documents, so that I can complete documents without carrying a laptop and reduce manual typing.

6. As a manager, I want the ability to switch between Vietnamese and English within the app, so that I can work comfortably in my preferred language.

7. As a manager, I want to add, edit, or remove options in certain drop-down lists (e.g., product names), so that the app can stay up to date when new fields are introduced.

## Functional Requirements
### Document Selection 
1.1. User views the document types (packing list, commercial invoice, stamp).

1.2. User selects document types.

### Assess Selected Page
2.1. User views the corresponding document input form after selecting a document type. 

2.2. User creates a new document using a predefined template.

2.3. User view and edit saved document.

### Input Validation
3.1. For Packing List

3.1.1. Platform requires “B/L No”, “Container No”, “Seal No”, “UNIT” must only contain capital letters, whole numbers and > 0. 

3.1.2. Platform requires date (i.e., “Date”, “B/L Date”) must follow DD/MM/YYYY format. 

3.1.3. Platform requires “Consignee”, “From”, “Description”, “Containers”, “Manufacture”,  to be a drop-down menu and fields can be added or removed. 

3.1.4. Platform requires  “QTY”, “Total IBC”, “QTY Liters” to only contain the whole number and > 0.

3.1.5. Platform requires “Gross Weight”, “CBM”, “GROSS WEIGHT KG” to only contain whole numbers, decimals and > 0.

3.1.6. Platform requires “NO” and “SHIP” to contain only capital letters, whole numbers, > 0 and special characters.

3.1.7. Platform requires “Email” and “Mobile” to be linked with “Consignee” so they can automatically be filled out after “Consignee” has been filled. 

3.1.8. Platform requires “Add” to be linked with “Manufacture” so they can automatically be filled out after “Manufacture” has been filled. 

3.1.9. Platform calculates total “QTY”, “QTY LITERS”, and “GROSS WEIGHT KG” and > 0 automatically. 

3.2. For Commercial Invoice: 

3.2.1. Platform requires “Customer”, “Terms”, field before “PORT” in “UNIT PRICE (AUD) FOB ____ PORT” and “AMOUNT (AUD) FOB ___ PORT” to be a drop-down menu and user can add or remove fields. 

3.2.2. Platform requires “Invoice No” to contain only capital letters, whole numbers, and > 0.

3.2.3. Platform requires “Unit Price”, “Amount” to contain only whole numbers, decimals and > 0. 

3.2.3. Platform requires “QTY” to contain only whole numbers and > 0. 

3.2.4. Platform requires “UNIT” to contain whole numbers, > 0, space and capital letters.

3.2.5. Platform requires “QTY OF LITER” to contain whole numbers, > 0 and special characters.

3.3.6. Platform requires “Email” and “Mobile” to be linked with “Customer” so they can automatically be filled out after “Customer” has been filled. 

3.1.9. Platform calculates total “AMOUNT (AUD) FOR ___ PORT” and “QTY OF LITER” and > 0 automatically.

3.3. For Stamp: 

3.3.1. Platform requires the last part of “Dầu nhớt động cơ đốt trong 4 kỳ…” in “Sản Phẩm”, “Nhãn hiệu”, “Nhập khẩu và phân phối”, “Nhà sản xuất” to be a drop-down menu and user can add or remove fields. 

3.3.2. Platform requires “Địa chỉ” to be linked with “Nhập khẩu và phân phối” and “Nhà sản xuất” so they can automatically be filled out after “Nhập khẩu và phân phối” and “Nhà sản xuất” has been filled. 

3.3.3. Platform requires “Đặc tính kĩ thuật: Cấp tính năng” to contain capital letters, whole number, > 0 and special characters. 

3.3.4. Platform requires “Cấp độ nhớt” to contain capital letters, whole number and > 0.

### Error Message Handling: 
4.1. Platform display a clear validation error message.

4.2. Platform highlights incorrect fields. 

4.3. Platform prevents progression until corrected. 

### Save Document: 
5.1. User save document before exporting.

### Export Options: 
6.1. User export document as PDF.

6.2. User export document as Word. 

6.3 The system display a confirmation page upon successful document export.

### Navigation: 
7.1. User click “Return” button to return to previous page.

7.2. User click “Home” button to return to Home page.

7.3. User exit the workflow safely.

### History Control: 
8.1. Platform stores only the most recent previous page to support the "Return to Previous Page" function.

## Non-functional Requirements
### Operational: 
1.1. Customers access the platform through an IOS platform.

1.2. Platform operates 24/7.

1.3. Platform has scheduled maintenance to implement updates.

1.4. Platform notifies customers a week in advance for maintenance. 

1.5. Platform provides a clean, mobile-friendly interface that can be used without training.

1.6. Platform automatically logs out inactive users after 15 minutes of inactivity.

1.7. Platform maintains at least 99% system availability during business hours.

### Performance: 
2.1. Platform responds to users’ actions within 1 second on average. 

2.1.1 Platform displays messages within 0.5 seconds.

2.2. Platform supports up to 5 users when they are on the app at the same time.

2.3. Platform load document templates within 2 seconds under normal network conditions.

2.4. Platform completes document export (PDF or Word) within 3 seconds.

2.5. Platform saves user input data without noticeable delay (less than 1 second).

### Security: 
3.1. Platform encrypts all stored documents and user data.

3.2. Platform uses HTTPS to secure data transmission.

3.3. Platform requires secure user authentication before granting access.

3.4. Platform enforces role-based access control (e.g., only managers can modify dropdown values).

3.5. Platform ensures that exported documents cannot be accessed by unauthorised users.

### Cultural and political requirements: 
4.1. Platform complies with Australian data protection and privacy regulations.

4.2. Platform ensures all content is culturally neutral and professional in tone.

4.3. Platform avoids discriminatory language, symbols, or imagery.

4.4. Platform supports English as the primary system language and Vietnamese as the secondary system language. 

4.5. Platform ensures date, currency, and number formats follow Australian standards (e.g., DD/MM/YYYY).

## Figma Prototype

The interactive prototype demonstrates the proposed user experience and document preparation workflow.

https://www.figma.com/proto/SLzaTWu6z6nDi8U47pJh18/Export-Docs-Automation-App?node-id=7-44&p=f&t=cdt4NBA39uwJYD3y-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=7%3A44

### Prototype Screens

## Figma Prototype

The interactive prototype demonstrates the proposed workflow for preparing export documents, managing predefined information, and supporting document processing through a mobile interface.

[View Interactive Figma Prototype](YOUR-FIGMA-LINK-HERE)

### Prototype Screens

#### First Screen

![First Screen](First%20Screen.png)

#### Log In Screen

![Log In Screen](Log%20In%20Screen.png)

#### Home Screen

![Home Screen](Home%20Screen.png)

#### Packing List Screen

![Packing List Screen](Packing%20List%20Screen.png)

#### Setting Screen

![Setting Screen](Setting%20Screen.png)

## Key Features

- Predefined document templates
- Drop-down menus
- Mandatory field validation
- Warning messages
- PDF and Word export
- Recent document storage
- Mobile-first interface
- English and Vietnamese language support

## Business Analysis Deliverables

- Project Scope Statement
- Project Charter
- Business Epic
- User Stories
- Functional Requirements
- Non-Functional Requirements
- Figma UI/UX Prototype

## Tools and Methodologies

- Figma
- Business Analysis
- Requirements Gathering
- User Stories
- Functional Requirements
- Non-Functional Requirements
- Project Scope Definition
- UI/UX Prototyping

## Prototype Limitations

The current Figma prototype is intended to demonstrate the proposed user experience rather than provide full application functionality.

Some functionality, including document storage, editable text input and complete bilingual support, would require application development beyond the Figma prototype.

## Disclaimer

This project is presented for portfolio purposes. Confidential company, customer, supplier and business information has been removed or anonymised.
