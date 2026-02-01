# Data-Virtualisation-Assignment
This repository contains the documentation deliverables for my individual Data Virtualization project built in Denodo. I designed an end-to-end virtualized reporting solution that integrates 7 retail CSV datasets into a single business-ready Reporting View (RV), then published it as a REST web service for lightweight downstream consumption.

#📌 Project Overview

Retail operations generate large volumes of sales and inventory data, but when stored across disconnected sources, decision-making becomes slow and error-prone.

This project builds a virtualized data model that consolidates transactional and inventory datasets into a single management-ready view. The result is a scalable architecture that enables:

Store-level performance tracking

Product & category sales analysis

Inventory health monitoring

Stock-to-sales ratio evaluation

REST-based real-time data access

The solution removes manual data consolidation and supports data-driven retail decisions.

#🏗 Architecture

The system follows a layered Denodo virtualization architecture:

CSV Sources
   ↓
Base Views (bv_*)
   ↓
Integrated Views (iv_*)
   ↓
Final Management View
   ↓
REST API Deployment

Data Sources

Orders

Order Items

Products

Categories

Stores

Stocks

Customers (extensible)

Brands (reference)

#🔧 Feature Engineering

Key engineered metrics include:

Total Sales Amount = quantity × price

Total Revenue per Product

Total Quantity Sold

Average Selling Price

Stock-to-Sales Ratio

Stock Status Classification

Derived time fields (year/month)

These transformations convert raw operational data into management-level KPIs.

#📊 Final Integrated View

The final virtualized dataset includes:

Category name

Product name

Store name

Total quantity sold

Total revenue

Current stock quantity

Stock-to-sales ratio

Stock health classification

This single view acts as a central analytics dataset for dashboards and reporting tools.

🌐 REST Deployment

The final view is deployed as a REST service using Denodo:

JSON / XML / HTML outputs

Pagination enabled for scalability

HTTP authentication for security

OpenAPI documentation auto-generated

This allows real-time consumption by dashboards and external systems without direct database access.

🎯 Business Impact

The virtualized model enables:

✔ Faster decision-making
✔ Reduced overstock & stockouts
✔ Improved inventory turnover
✔ Better revenue visibility
✔ Scalable analytics architecture
