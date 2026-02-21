# 🏋 Gym Management System (Zoho Creator)

A Gym Management Application developed using Zoho Creator with automated membership expiry tracking and status management.

---

## 🚀 Features

- Member Registration with Photo Upload
- Membership Plan Selection
- Fee Amount 
- Automatic Expiry Date Calculation
- Dynamic Active / Expired Status Update
- Membership End Date Display
- Organized Member Records

---

## 🛠 Technology Used

- Zoho Creator (Low-Code Platform)
- Deluge Scripting
- Form-Based Database Design
- Workflow Automation

---

## 🔄 Business Logic Implemented

- Expiry Date auto-calculated based on Join Date and Membership duration
- Status automatically changes to "Expired" after expiry date
- Active members displayed dynamically

---
Code:-
if(input.Join_Date != null)
{
    if(input.Membership_Plan == "Monthly")
    {
        input.Expiry_Date = input.Join_Date.addMonth(1);
    }
    else if(input.Membership_Plan == "3 Months")
    {
        input.Expiry_Date = input.Join_Date.addMonth(3);
    }
    else if(input.Membership_Plan == "6 Months")
    {
        input.Expiry_Date = input.Join_Date.addMonth(6);
    }
    else if(input.Membership_Plan == "1 Year")
    {
        input.Expiry_Date = input.Join_Date.addYear(1);
    }
}

if(input.Expiry_Date != null)
{
    if(input.Expiry_Date < zoho.currentdate)
    {
        input.Status = "Expired";
    }
    else
    {
        input.Status = "Active";
    }
}

## 📷 Screenshots

Project screenshots are available inside the `/screenshots` folder.

---

## 📌 Project Purpose

This project demonstrates:

- Real-world membership lifecycle management
- Date-based automation logic
- Low-code application development
- Business process automation using Deluge

---

## 👨‍💻 Developer

Sumit Prasad
