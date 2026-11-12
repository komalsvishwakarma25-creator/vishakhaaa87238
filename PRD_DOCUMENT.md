Rural360

Complete PRD & Antigravity Development Plan

“From Customer Conversations to Smarter Business Decisions.”

1. Product Overview

Rural360 is an AI-powered Customer Intelligence and Business Decision Support Platform designed for rural entrepreneurs. It converts customer conversations, complaints, reviews, sales, inventory and customer behavior into simple business insights, explains possible reasons behind business changes, and recommends practical next actions.

Core product flow:

Customer Conversations → Customer Feedback → Business Data → AI Analysis → WHY Engine → Business Insights → Action Recommendations → Smart Alerts

2. Core Problem

Rural entrepreneurs may have access to digital commerce and communication tools, but their business information can remain fragmented. They may know sales, revenue, complaints and reviews, but still struggle to understand why sales change, why customers become unhappy, which customers need attention, which products to restock, and what action to take next.

Rural360 addresses this gap through:

Data → Understanding → WHY → Insight → Recommendation → Action

3. Target Users

Primary: Rural entrepreneurs such as handicraft sellers, farmer-producers, homemade food sellers, artisans, weavers, and small shop owners.

Secondary: Customers who ask questions, provide feedback, register complaints and track complaint status.

Admin: Platform administrator managing users, businesses, complaints, reports and system settings.

4. Core Product Modules

Customer Care

Customer Intelligence

Business Insights

WHY Engine

AI Business Mentor

Smart Alerts

Growth Dashboard

5. Customer Care

Objective: Provide simple, multilingual and intelligent customer support.

AI chatbot for product availability, pricing, delivery, returns and business policies.

English, Hindi and Marathi-ready interface with architecture for additional languages.

Voice input and voice-response-ready interaction.

Complaint registration and ticket tracking.

Feedback collection and customer ratings.

Conversation history and support status.

Complaint workflow: Open → In Progress → Resolved

6. Customer Intelligence

For every customer calculate:

Total orders and total spending.

Average order value and purchase frequency.

Last purchase date.

Complaint count and average rating.

Customer status.

Automatically classify customers as:

New

Repeat

High Value

Inactive

At Risk

7. Customer Emotion / Feedback Analyzer

Analyze reviews, complaints and feedback to identify sentiment and major topics.

Sentiment: Positive, Neutral, Negative, or Mixed.

Topics: Product Quality, Price, Packaging, Delivery, Customer Service, Availability.

Example: “Product quality is very good but delivery was very late.” The system identifies Product Quality as Positive, Delivery as Negative, and Overall Sentiment as Mixed.

8. Business Insights

The dashboard should calculate and display:

Daily sales, weekly sales and monthly revenue.

Total orders, new customers and repeat customers.

Customer satisfaction and complaint resolution.

Best-selling, slow-moving, most profitable and low-stock products.

Product demand trends and inventory status.

9. WHY Engine

The WHY Engine is the main innovation layer. Instead of only showing WHAT happened, it investigates available business data and explains possible contributing reasons.

Example:

Sales ↓ 18% → Repeat Customers ↓ 12% → Negative Reviews ↑ 18% → Delivery Complaints ↑ 32% → Possible contributing factor: delivery delays.

Output structure: WHAT HAPPENED → WHY IT MAY HAVE HAPPENED → EVIDENCE → RECOMMENDED ACTION.

Important: Never present correlation as proven causation. Use language such as “possible contributing factor”, “associated with”, or “may be affecting”. Show supporting metrics.

10. AI Business Mentor

A conversational business assistant that answers questions using the authenticated entrepreneur’s own data.

Why are my sales decreasing?

Which product sells the most?

Which customers should I contact?

What are customers complaining about?

What should I restock?

How is my business performing this month?

Flow: User Question → Intent Detection → Retrieve Relevant Business Data → Calculate Metrics → AI Interpretation → Answer.

11. Voice Business Assistant

Allow entrepreneurs to ask questions by voice, such as “Mere business mein iss month kya problem hai?” or “Aaj kitne orders aaye?” Convert speech to text, process it through the Business Mentor, and return a simple response.

12. Smart Alerts

Low inventory.

Pending complaints.

Unanswered customer queries.

Sales increase or decrease.

Customer satisfaction decrease.

Inactive high-value customers.

Repeat customer opportunities.

Seasonal demand.

Payment issues.

Each alert should contain: title, severity, reason, supporting metric, recommended action, timestamp, and read/unread status.

13. Proactive Customer Support

Traditional: Customer Complaint → Entrepreneur Responds

Rural360: Customer Data → AI Detects Pattern → Potential Problem → Predict Risk → Alert Entrepreneur → Take Action

Example: “Early Warning: Delivery complaints have increased by 25% this week.”

14. Festival Demand Insights

Use historical sales and configurable festival dates to identify relevant products and seasonal patterns. Example: If previous Diwali basket sales were approximately 45% higher than normal, the system can suggest preparing additional stock.

Clearly label this as historical-based guidance, not a guaranteed prediction.

15. AI Business Simulator

Allow entrepreneurs to test hypothetical decisions such as price reductions, discounts, inventory changes or offers.

Example: “What if I reduce the price by 10%?” Show current scenario, hypothetical scenario, historical comparison and estimated impact.

Clearly label all outputs as ESTIMATES and show assumptions. Never present simulations as guaranteed predictions.

16. Growth Dashboard

Create a transparent Business Health Score from 0–100 using:

Sales Growth

Customer Satisfaction

Customer Retention

Complaint Resolution

Inventory Health

Show the score, individual component scores, trend over time, reasons for changes, and recommended actions.

17. Business Story

Create a “Your Business This Month” summary answering:

What improved?

What declined?

What needs attention?

Which products performed well?

Which customers need attention?

What are the recommended next actions?

Keep the language simple and prepare the architecture for English, Hindi and Marathi.

18. Growth Roadmap

Generate a personalized 30-day action plan based on current business insights.

Resolve pending complaints.

Contact inactive customers.

Restock best-selling products.

Review delivery complaints.

Allow the entrepreneur to mark actions complete, postpone, dismiss, and view why an action was recommended.

19. Main Application Screens

Entrepreneur:

Dashboard

Customer Care

Customers

Customer Intelligence

Products

Orders

Business Insights

WHY Engine

AI Business Mentor

Smart Alerts

Growth Dashboard

Reports

Settings

Customer:

Home

Products

Product Details

Orders

AI Support

Complaints

Feedback

Admin:

Admin Dashboard

Users

Businesses

Complaints

Analytics

Settings

20. Database Structure

Users: id, name, phone, email, role, language, createdAt.

Businesses: id, ownerId, businessName, category, location, description.

Products: id, businessId, name, description, price, stock, category.

Orders: id, customerId, businessId, items, totalAmount, status, createdAt.

Customers: id, businessId, name, phone, location, totalOrders, totalSpent, lastPurchase.

Complaints: id, customerId, businessId, orderId, issue, priority, status, createdAt, resolvedAt.

Feedback: id, customerId, productId, rating, review, sentiment, topics, createdAt.

Insights: id, businessId, type, title, description, severity, recommendation, createdAt.

Alerts: id, businessId, type, message, priority, isRead, createdAt.

21. Technical Architecture

Web / Mobile UI → React / PWA → API Layer → Node.js / Backend → Database + AI Layer + Authentication → Insight Engine → WHY Engine → Recommendations → Smart Alerts

Recommended stack: React.js/PWA for frontend, Node.js/Express for backend, PostgreSQL or MongoDB for data, Firebase/Auth for authentication where appropriate, Chart.js or Recharts for visualizations, and a secure LLM/API integration for AI.

22. AI Architecture Principles

Do not let the LLM invent business numbers. Use the database and analytics engine to calculate metrics first, then use AI to interpret those verified metrics and generate recommendations.

Example flow: Database → Analytics Engine → Calculated Metrics → AI Interpretation → Recommendation.

23. Security Requirements

Authentication and role-based access control.

Business-level data isolation.

Secure API endpoints and input validation.

Rate limiting and secure file uploads.

Secrets must never be exposed in frontend code.

AI prompt-injection protection and controlled data retrieval.

Audit logs and secure error handling.

Entrepreneur A must never be able to access Entrepreneur B’s business or customer data.

24. Antigravity Step-by-Step Development Plan

Phase 1 — Project Foundation: Create scalable frontend, backend, database layer, authentication, routing, reusable components, API structure, environment configuration, error handling and role-based access control. Do not implement advanced AI yet.

Phase 2 — UI/UX: Build responsive entrepreneur, customer and admin screens. Use large touch targets, simple navigation, multilingual-ready architecture, realistic sample data, accessible typography and mobile-first design.

Phase 3 — Authentication: Implement registration, login, logout, protected routes, session persistence, role-based navigation and authorization.

Phase 4 — Database: Create Users, Businesses, Products, Customers, Orders, OrderItems, Complaints, Feedback, CustomerInteractions, Insights, Alerts, BusinessMetrics and AIRecommendations with relationships, indexes and demo data.

Phase 5 — Customer Care: Implement AI-ready chatbot UI, FAQ, questions, complaints, ticket tracking, feedback, ratings, conversation history and multilingual-ready support.

Phase 6 — Customer Intelligence: Calculate customer metrics and classify customers as New, Repeat, High Value, Inactive and At Risk.

Phase 7 — Feedback Intelligence: Implement sentiment and topic analysis for reviews, complaints and feedback. Provide a deterministic mock layer if an AI API is unavailable.

Phase 8 — Business Analytics: Calculate daily/weekly/monthly sales, revenue, orders, average order value, customer growth, product performance, inventory and satisfaction from real database records.

Phase 9 — WHY Engine: Build evidence-based root-cause exploration using sales, customers, complaints, sentiment, inventory and product performance. Distinguish correlation from causation.

Phase 10 — AI Business Mentor: Build a conversational assistant that retrieves relevant authenticated business data, calculates metrics, interprets them, and answers business questions.

Phase 11 — Voice Assistant: Add speech-to-text business queries with graceful fallback to text.

Phase 12 — Smart Alerts: Create rule-based alerts for inventory, complaints, queries, sales changes, satisfaction, inactive customers, repeat-customer opportunities, seasonal demand and payments.

Phase 13 — Festival Demand Insights: Use historical sales and configurable festival dates to generate clearly labeled historical-based guidance.

Phase 14 — AI Business Simulator: Allow hypothetical price, discount, inventory and offer scenarios. Show estimates and assumptions.

Phase 15 — Business Health Score: Implement transparent 0–100 scoring using sales growth, satisfaction, retention, complaint resolution and inventory health.

Phase 16 — Business Story: Generate a simple monthly summary of improvements, declines, attention areas, products, customers and recommended actions.

Phase 17 — Growth Roadmap: Generate and track a personalized 30-day action plan.

Phase 18 — Reports: Generate monthly, sales, customer, complaint, inventory and sentiment reports with PDF/CSV export where supported.

Phase 19 — Admin: Implement user, business, product, complaint, feedback, AI configuration, category and language management with audit logs.

Phase 20 — UI Polish: Audit every screen for spacing, typography, navigation, responsive behavior, accessibility, loading/empty/error states and information density.

Phase 21 — Security Audit: Test authentication, authorization, data isolation, API validation, database security, file uploads, rate limiting, secrets management and AI prompt-injection protection.

Phase 22 — Final QA: Test all end-to-end flows, fix functional bugs and verify calculations, API/database behavior, responsive UI and permissions.

25. Antigravity Master Development Prompt

Use the following principles across all Antigravity phases: inspect the existing repository before changing it; reuse components where appropriate; keep the architecture modular; never fabricate business metrics; protect tenant data; provide loading, empty and error states; keep AI outputs grounded in retrieved business data; label estimates clearly; avoid claiming correlations are proven causes; and prioritize simplicity for rural entrepreneurs.

26. Final Product Architecture

Customer Side: Chat / Voice / Orders / Feedback / Complaints → Customer Intelligence.

Entrepreneur Side: Dashboard / Customer Care / Customers / Products / Orders / Business Insights / WHY Engine / AI Mentor / Smart Alerts / Growth Dashboard.

Intelligence Layer: Sentiment Analysis + Analytics Engine + Customer Segments → WHY Engine → Possible Reasons → Recommendations → Smart Actions.

27. Final USP

Do not position Rural360 as simply a website where rural entrepreneurs sell products. Position it as an AI-powered Customer Intelligence and Business Decision Support Platform.

Core differentiating flow: Customer Interaction → AI Understanding → WHY Analysis → Business Insight → Recommendation → Action.