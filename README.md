# Bartan-Store-POS

## 🏪 Overview
This project is an Automated Point of Sale (POS) system built using N8N, designed specifically for Bartan Store businesses to manage inventory and invoices seamlessly.  It automates record-keeping, stock updates, invoice generation, and even sends professional invoices directly to customers via Gmail.
# 🧾 Abdullah Bartan Store POS – n8n Workflow Automation

---

## ⚙️ Key Features

### 🧠 Intelligent Inventory Management
- Automatically generates **Product Codes** (e.g., `BS-001`, `BS-002`, …)
- Adds, updates, or deletes products easily  
- Auto-updates stock when a product is sold  
- Sends **low-stock alerts** when quantity drops below 40  

### 🧾 Smart Invoice System
- Generates **Invoices Automatically** with unique numbers:  
  Format → `INV-YYYYMMDD-HHMMSS`
- Auto-fills **Date** and **Invoice Number**
- Prompts for required fields:
  - Customer Name  
  - Customer Email  
  - Product Name  
  - Quantity  
  - Customer Phone  
  - Customer Address
- Automatically **reduces stock** in the inventory when invoices are created  
- Sends **professional invoices** to customers via the **Gmail Node**

### 📧 Email Automation (via Gmail Node)
Each invoice is sent in a **structured and professional format** with the following details:

| Product Name        | Category         | Quantity |
|---------------------|------------------|----------|
| Glass Water Jug     | Glass Crockery   | 2        |

---

## 📂 Sheets Overview

### 🗂️ Inventory Sheet
| Product Inventory | Product Name      | Product Category   | Stock Available |
|-------------------|------------------|--------------------|----------------|
| BS-001            | Steel Plate      | Steel              | 120            |
| BS-002            | Glass Water Jug  | Glass Crockery     | 95             |

**Rules:**
- Auto-generate next sequential product code  
- Update stock when products are sold or restocked  
- Alert if stock < 40  

---

### 🗂️ Invoices Sheet
| Date       | Invoice Number         | Customer Name | Customer Email     | Product Name       | Quantity | Customer Phone | Customer Address      |
|-------------|------------------------|----------------|--------------------|--------------------|-----------|----------------|------------------------|
| 2025-09-23 | INV-20250923-142315    | Ali Khan       | ali@example.com    | Glass Water Jug    | 2         | 03001234567    | Lahore, Pakistan       |

**Rules:**
- Auto-generate Date and Invoice Number  
- Auto-update stock in the Inventory sheet  
- Send invoice to Customer via Gmail Node  

---

## 📤 Automated Outputs

### ✅ Inventory Update Example
✅ Inventory Updated
Product Code: BS-011
Product Name: Glass Water Jug
Category: Glass Crockery
Stock Available: 95

shell
Copy code

### ✅ Invoice Example (sent to Gmail)
📑 Abdullah Bartan Store
123 Main Street, Lahore, Pakistan
Phone: +92 300 1234567 | Email: support@bartanstore.com

INVOICE
Date: 2025-09-23
Invoice Number: INV-20250923-142315
Bill To:
Customer Name: Ali Khan
Email: ali@example.com
Phone: 03001234567
Address: Lahore, Pakistan

Product Details:

Product Name	Category	Quantity
Glass Water Jug	Glass Crockery	2

Thank you for shopping with Abdullah Bartan Store.
Please contact us if you have any questions regarding your order.

yaml
Copy code

---

## 🧩 Nodes Used in Workflow

| Node Type           | Purpose |
|----------------------|----------|
| **Google Sheets**    | Manage Inventory & Invoices data |
| **Gmail Node**       | Send structured invoices to customers |
| **Set Node**         | Format invoice data |
| **Function Node**    | Generate unique product/invoice codes |
| **IF Node**          | Handle low stock alerts |
| **AI Agent Node**    | Process user queries and manage logic |
| **Webhook/Trigger Node** | (Optional) For future WhatsApp Assistant integration |

---

## 🔮 Future Enhancements (V2)

- 💬 WhatsApp Assistant integration for managing invoices and inventory via chat  
- 📊 Dashboard with sales summary and inventory analytics  
- 🧾 PDF invoice attachment via Gmail  
- 🔔 Auto-daily report to store owner’s email  

---

## 🚀 How to Use

1. Upload `Bartan Store.xlsx` to Google Drive and connect it with n8n Google Sheets node.  
2. Import this n8n workflow into your workspace.  
3. Connect the **Gmail Node** with your Gmail account for automated invoice delivery.  
4. Run the workflow manually or trigger through an input (AI Agent or Form).  
5. The workflow will:
   - Create invoices  
   - Update inventory  
   - Send invoice email  
   - Track all changes automatically  

---

## 📜 License
This project is released under the **MIT License**. You’re free to use, modify, and share it for personal or commercial use.

---

## 📞 Contact
**Developer:** Abdullah Shahzad  
📧 Email: support@xpertswp.com  
📧 Email: shahzadabdullah37@gmail.com
🌐 Website: https://xpertswp.com
💡 If you need a custom automation system for your business — Let’s collaborate!

---

### ⭐ Don’t forget to star this repo if you find it helpful!
