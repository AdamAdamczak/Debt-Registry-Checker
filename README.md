# Checking Proceedings on KRZ

## Project Description
This project automates the process of checking proceedings on the [KRZ](https://krz.ms.gov.pl/#!/application/KRZPortalPUB/1.9/KrzRejPubGui.WyszukiwaniePodmiotow?params=JTdCJTdE&seq=0) website for individuals running business activities. The search is done using either a NIP (Tax Identification Number) or PESEL (Personal Identification Number), and the following information is retrieved:
- Type of proceedings
- Signature and link to the signature

The automation is implemented using **UiPath** and managed via **Orchestrator**.

## Input
The robot receives input in the form of:
- **An item in the queue** added through the UiPath Orchestrator API, containing the **NIP/PESEL number** to search for.

## Output
After processing the transaction, the result is saved as:
- **Status in the Output transaction in the queue**
- Option to generate an **Excel report** with the proceedings data

## Technologies Used
- **UiPath Studio** – for building the automation
- **UiPath Orchestrator** – for managing queues and executing processes
- **Excel** – for reporting results (optional)

## How to Run the Project
1. **Upload** files to UiPath Orchestrator.
2. **Configure** the queue in Orchestrator.
3. **Add** items to the queue via the API (with NIP/PESEL numbers).
4. **Run** the process in Orchestrator.
5. **Read** the results from the Output transaction in the queue or download the Excel report.
