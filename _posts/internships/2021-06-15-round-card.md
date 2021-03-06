---
layout: post
title:  "Summer Internship at Rocky Core: IC Cards and Security"
description: "Building applications for integrated-circuit cards, and implementing security mechanisms using cryptographic algorithms such as AES and RSA."
image: "/assets/img/rockycore/rockycore-logo.jfif"
time: "June - July 2021"
categories: internship
tag: internship
---

Over the summer of 2021, I had the honor of joining Rocky Core as an intern, where I had the chance to explore a new industry that I never knew much about before. I was able to gain a better understanding of internet security and of cryptography, as well as their implementation on microchips and smart cards. I also learned about some of the key services that Rocky Core provides. In this post I will document my experience there.

### About the Company

Rocky Core is a tech startup that focuses on internet security on mobile devices and the IoT. Using integrated circuit (IC) cards, secure elements (SE) and Java Card operating systems, it aims at building a safe environment for highly sensitive data to be stored, transferred, and utilized. The application of their products ranges from bus passes, to mobile phones, and to financial products.

### My Experience

At Rocky Core, I was exposed to a new field that was very different from what I had experienced before--integrated circuit (IC) cards and secure elements (SE). 

My internship lasted six weeks from June 2021 to July 2021. It was divided into three stages:

**1. Learning new materials (1 weeks)**

- The ISO7816-4 standardization for integrated circuit cards
- Java Card framework and API
- The basic framework for IC card development
- Cryptography:
    - Cipher algorithms like DES, AES, and RSA
    - Signature algorithms
    - Message authentication code (MAC)

**2. Building applications (3 weeks)**

- A file system that complies with the ISO7816-4 document
- An electronic purse (EPurse) application
- A smart lock application

**3. More on the Java Card System (2 weeks)**

- Java Card Operating System
- Java Card Virtual Machine
- Java Card Runtime Environment
- Java Card application workflow
- Global Platform Specification

Some of my notes are included below:

## Stage I: Learning new materials

I began my internship by familiarizing myself with some of the essential documents for the field of IC card development. This is certainly something I did not know before--that the industry of smart chips is essentially built around a whole series of standards. Without these standards, our chips and cards would not be so widely used as they are today. One of the most critical documents of the field is <a href="https://www.iso.org/standard/54550.html">**ISO7816-4**</a>, put together by the International Organization for Standardization (ISO) for the purpose of standardizing the IC card industry. It dictates the essential commands (APDU commands) that a card should support, the structure of its file system, and so on. From this document, I learned of the basic structures of Java Card applications, and how various components of such an application are joined together into one workflow. I cross-referenced these pieces of information with the Java Card API to gain a better understanding of how an application is put together.

Another vary important part of my learning centers around **cryptography**. Nowadays we encounter smart cards that demand a high level of security, from bus passes, to hotel keys, to credit cards. In order to keep the information stored in these cards secure, cryptography and the various cipher algorithms play a very important role.

### Some of the concepts of cryptography that I learned about
- Symmetric vs. unsymmetric keys
- Cipher Block Chaining (CBC) vs. Electronic Codebook (ECB)
- Message Authentication Code (MAC)
- Algorithms:
  - Data Encryption Standard (DES)
  - Advanced Encryption Standard (AES)
  - RSA
  - ECC256 and ECDSA

## Stage II: Building small applications!

As I familiarized with the specifications of ISO7816-4, I began exploring some small applications. The first project I worked on was to build a file system, and of course, it had to comply with the ISO standard. As designated by ISO7816-4, a smart card file system is made up of three kinds of file structures: the MF, DF, and EF.

### **Building a file system**

After learning about the standards, I began designing and building a file system for IC cards, in compliance with ISO7816-4. Based on the standards of ISO7816-4, an integrated circuit card should support three file types:
1. **MF file** - This is the highest directory of the file system, or we can think of it as the root directory. There can only be one MF in a given card, and the MF can contain many other files of the other two file types.
2. **DF file** - A DF includes system information and application-related settings. There are two types of DFs: 1) ADF, which can only hold EF files, and 2) DDF, which can hold other DFs under itself.
3. **EF file** - An EF is at the bottom of the file system, and it encodes information like user data and internal data.

Some of the supported instructions include:
- Create file
- Select file
- Write binary file
- Read binary file
- Write record
- Read record
- etc.

### **Electronic purse (EPurse)**

Having learned the basic structure of a Card OS file system, I then moved on to build an electronic purse application, in compliance with the China Financial Integrated Circuit Card Specifications.

This application was essentially structured around the same file system as above, but with one critical distinction: this EPurse application requires strict compliance with a set of security requirements, limiting the access permission of each file. Moreover, this application made use of a larger set of instructions, bringing in a wider range of authentication instructions as well as instructions specific to commercial interactions.

Some of the new instructions include:
- Verify pin: authentication using the PIN
- Application block: block the application after the number of authentication failures exceeds a certain threshold
- Initialize for load and credit for load: these two instructions are for loading money into the account
- Initialize for purchase and debit for purchase: these two instructions are for establishing purchases
- Get balance: read the balance of the account 