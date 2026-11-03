# Datheon OOPS & System Design Internship Tasks

This repository contains the complete implementation of core Object-Oriented Programming (OOP) principles, SOLID software design, standard Design Patterns, and Low-Level System Design (LLD) as part of the Datheon Internship Program.

---

## 📌 Project Overview & Completed Tasks

### Task 1: The 4 Pillars of OOP: Multi-Currency Banking & Ledger Engine
* **Goal**: Demonstrate strict Encapsulation, Inheritance, Polymorphism, and Abstraction.
* **Key Components**:
  * **Abstraction**: Abstract `Account` base class defining core interfaces for `accrue_interest()` and `deduct_fees()`.
  * **Encapsulation**: Private attributes with strict property getters and input validation guards.
  * **Inheritance**: Specialized implementations for `SavingsAccount`, `CheckingAccount` (with overdraft protection), and `HighYieldAccount`.
  * **Polymorphism**: Unified `LedgerEngine` handling atomic inter-account transfers and end-of-month batch settlements.

---

### Task 2: SOLID Principles: Notification & Alert Dispatch Framework
* **Goal**: Build an extensible alert dispatch library following all 5 SOLID principles.
* **Key Components**:
  * **Single Responsibility Principle (SRP)**: Distinct decoupling between message payloads, delivery channels, and the dispatch manager.
  * **Open/Closed Principle (OCP)**: Pluggable channel architecture allowing new integrations (e.g., Telegram, Webhooks) without modifying the core dispatcher.
  * **Liskov Substitution Principle (LSP)**: All providers (`Email`, `SMS`, `Slack`, `WhatsApp`) adhere strictly to the `NotificationChannel` base contract.
  * **Interface Segregation Principle (ISP)**: Lean channel interface definitions.
  * **Dependency Inversion Principle (DIP)**: Channels injected directly into the high-level `NotificationDispatcher` service via Dependency Injection.

---

### Task 3: Creational & Behavioral Design Patterns: E-Commerce Order Pipeline
* **Goal**: Implement standard creational and behavioral design patterns in an end-to-end order workflow.
* **Key Components**:
  * **Singleton Pattern**: Thread-safe `DatabaseConfigManager` maintaining unified system configuration and logging.
  * **Factory Method Pattern**: `PaymentHandlerFactory` instantiating polymorphic handlers (`CreditCard`, `UPI`, `PayPal`, `Crypto`).
  * **Observer Pattern**: Dynamic event-driven architecture broadcasting order lifecycle updates (`PLACED`, `PAID`, `PACKED`, `DISPATCHED`) to `LogisticsService`, `InvoiceService`, and `EmailNotificationService`.

---

### Task 4: Low-Level System Design (LLD): Smart Parking Lot Architecture
* **Goal**: Design and implement a robust multi-floor smart parking facility from scratch.
* **Key Components**:
  * **Vehicle Hierarchy**: Support for `Motorcycle`, `CompactCar`, `LargeSUV`, and `ElectricVehicle`.
  * **Automated Slot Allocation**: Floor-by-floor allocation algorithm matching vehicle specifications with compatible slot types.
  * **Ticket & Lifecycle Management**: Unique ticket issuance and spot occupancy tracking.
  * **Dynamic Pricing Engine**: Automated hourly rate calculation with dedicated surcharges based on vehicle category and charging requirements.

---

## 🚀 Tech Stack & Requirements

* **Language**: Python 3.8+
* **Environment**: Google Colab / Jupyter Notebook / Local Python CLI
* **Modules Used**: `abc`, `enum`, `threading`, `datetime`, `dataclasses`, `typing`

---

## 💻 How to Run the Code

1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/<your-repo-name>.git
