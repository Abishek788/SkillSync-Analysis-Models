
Skillsync analysis models · MD
Copy

# SkillSync-Analysis-Models

**SkillSync: Analysis Models & Architectural Design**

## Project Overview

SkillSync is a decentralized, peer-to-peer learning network designed to bridge the gap in vocational training. The platform connects "Learners" with local "Mentors" (experts in trades like carpentry, plumbing, and automotive repair) for in-person, hands-on instruction.

This repository contains the analysis models that define the system's requirements and preliminary data architecture.

---

## 1. UML Use Case Diagram

The Use Case diagram defines the functional scope of the SkillSync platform by identifying how different users (Actors) interact with the system.

### Actors

- **Learner**: The primary consumer looking to acquire new trade skills.
- **Mentor**: The subject matter expert providing instruction and listing skills.
- **Tool Owner**: A specialized user who may rent out workshops or physical tools.
- **Admin**: Oversees system integrity, identity verification (KYC), and dispute resolution.
- **Payment Gateway**: An external system actor that handles escrow and financial transactions.

### Key Use Cases

- **Skill Bartering**: A unique engagement feature allowing users to trade skills directly without monetary exchange.
- **Identity Verification**: A critical security requirement where Admins verify the credentials and safety of participants.
- **Escrow Processing**: Ensures payments are held securely until the learning session is marked complete by both parties.

---

## 2. UML Class Diagram

The Class Diagram defines the static structure of the SkillSync database and the relationships between various objects.

### Core Architecture

- **Inheritance Hierarchy**: A base `User` class contains common attributes (ID, email, rating). This is specialized into `Learner`, `Mentor`, and `ToolOwner` subclasses, allowing for modular role management.

- **The Session Object**: This serves as the central "glue" of the system. It associates a Learner and a Mentor at a specific time and location, while linking directly to a Payment transaction and a potential Review.

- **Data Composition**: The `Mentor` class has a "one-to-many" relationship with `Skills`, ensuring that an expert can be listed for multiple specialties (e.g., a Mentor who teaches both plumbing and basic electrical work).

---

## Development Context

These models were developed using the **Agile SCRUM methodology**. As a project manager, these artifacts provide our development team with the necessary logic to begin the preliminary design of the API and database schema.

**Project Manager / Scrum Master**: Abishek kc  
**Date**: February 2026
