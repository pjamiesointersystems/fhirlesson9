### Be sure to run first the file fhirsurgerybatchwithObservations.http to get new surgery patients with observations


# FHIR Lesson 9: Search and FHIRPath in Clinical Problem Solving

Welcome to Lesson 9 of the InterSystems FHIR Curriculum. This module is designed to teach practical applications of **FHIR Search** and **FHIRPath** through engaging clinical problem-solving scenarios. Students will gain hands-on experience constructing search queries, analyzing FHIR bundles, and extracting meaningful clinical insights using Python and Jupyter Notebooks.

---

## 🧠 Learning Objectives

By the end of this lesson, students will be able to:

- Construct FHIR RESTful search queries using standard parameters and value sets.
- Apply FHIRPath expressions to extract and filter data from FHIR resources.
- Use Python to access and analyze FHIR server responses.
- Translate clinical problems into data queries and perform real-time analysis.
- Compare datasets and derive insights using programmatic logic.

---

## 🏥 Clinical Scenario: Preventing Type 2 Diabetes

Nurse Emily Carter, a diabetes specialist at Fairway Hospital, is tasked with identifying patients at risk for developing Type 2 Diabetes. Using FHIR-based tools, she investigates patterns in Hemoglobin A1c (HbA1c) lab results and condition codes to stratify patient risk. This scenario simulates her work and challenges students to reproduce her queries and analyses.

---

## Populate the FHIR Repository with Surgical Patients

Problem 7, requires analyzing patients with surgical conditions. Execute the POST command in fhirsurgbatch.http,
a transaction batch file, first with the command POST http://127.0.0.1:8080/csp/healthshare/demo/fhir/r4 to populate surgical procedures and their patients
Next executute the POST command in fhirsurgbatchobs.http, a simple batch file, with the command POST POST http://127.0.0.1:8080/csp/healthshare/demo/fhir/r4. THis file contains additional observations on these surgical patients. 
These commands only need to be executed once, but without them you won't be able to find any surgical patients.





---

## 🔍 Key Topics Covered

- **FHIR Search Basics**  
  E.g., `Patient?gender=female` or `Observation?code=4548-4&value-quantity=ge6.0`

- **FHIRPath Essentials**  
  E.g., `Patient.name.given`, `Observation.valueQuantity.value`

- **Use of SNOMED and LOINC codes**  
  E.g., SNOMED `15777000` for prediabetes; LOINC `4548-4` for HgbA1c

- **Combining Python + FHIRPath**  
  Execute and post-process search results using Python for sorting, comparison, and visualization.

---

## 🧪 Problem Set Highlights

1. **Find all patients with prediabetes** using the appropriate SNOMED code.
2. **Retrieve HgbA1c observations** for a specific patient.
3. **Extract and sort values** using FHIRPath and Python.
4. **Apply filters** to search results (e.g., `value-quantity=ge6.0`).
5. **Compare cohorts** based on lab values vs condition codes.

Additional problems introduce **PreventHF**, a startup using FHIR to monitor CHF patients, applying similar techniques to track weight fluctuations and prevent readmission.

---

## 🛠 Requirements

To run the lesson locally, install the following Python packages:

```bash
pip install requests fhir.resources matplotlib

---

## 🔍 Key Topics Covered

- **FHIR Search Basics**  
  E.g., `Patient?gender=female` or `Observation?code=4548-4&value-quantity=ge6.0`

- **FHIRPath Essentials**  
  E.g., `Patient.name.given`, `Observation.valueQuantity.value`

- **Use of SNOMED and LOINC codes**  
  E.g., SNOMED `15777000` for prediabetes; LOINC `4548-4` for HgbA1c

- **Combining Python + FHIRPath**  
  Execute and post-process search results using Python for sorting, comparison, and visualization.

---

## 🧪 Problem Set Highlights

1. **Find all patients with prediabetes** using the appropriate SNOMED code.
2. **Retrieve HgbA1c observations** for a specific patient.
3. **Extract and sort values** using FHIRPath and Python.
4. **Apply filters** to search results (e.g., `value-quantity=ge6.0`).
5. **Compare cohorts** based on lab values vs condition codes.

Additional problems introduce **PreventHF**, a startup using FHIR to monitor CHF patients, applying similar techniques to track weight fluctuations and prevent readmission.

---

## 🛠 Requirements

To run the lesson locally, install the following Python packages:

```bash
pip install requests fhir.resources matplotlib

---

## 🔍 Key Topics Covered

- **FHIR Search Basics**  
  E.g., `Patient?gender=female` or `Observation?code=4548-4&value-quantity=ge6.0`

- **FHIRPath Essentials**  
  E.g., `Patient.name.given`, `Observation.valueQuantity.value`

- **Use of SNOMED and LOINC codes**  
  E.g., SNOMED `15777000` for prediabetes; LOINC `4548-4` for HgbA1c

- **Combining Python + FHIRPath**  
  Execute and post-process search results using Python for sorting, comparison, and visualization.

---

## 🧪 Problem Set Highlights

1. **Find all patients with prediabetes** using the appropriate SNOMED code.
2. **Retrieve HgbA1c observations** for a specific patient.
3. **Extract and sort values** using FHIRPath and Python.
4. **Apply filters** to search results (e.g., `value-quantity=ge6.0`).
5. **Compare cohorts** based on lab values vs condition codes.

Additional problems introduce **PreventHF**, a startup using FHIR to monitor CHF patients, applying similar techniques to track weight fluctuations and prevent readmission.

---

## 🛠 Requirements

To run the lesson locally, install the following Python packages:

```bash
pip install requests fhir.resources matplotlib
## 🔍 Key Topics Covered

- **FHIR Search Basics**  
  E.g., `Patient?gender=female` or `Observation?code=4548-4&value-quantity=ge6.0`

- **FHIRPath Essentials**  
  E.g., `Patient.name.given`, `Observation.valueQuantity.value`

- **Use of SNOMED and LOINC codes**  
  E.g., SNOMED `15777000` for prediabetes; LOINC `4548-4` for HgbA1c

- **Combining Python + FHIRPath**  
  Execute and post-process search results using Python for sorting, comparison, and visualization.

---

To run the lesson locally, install the following Python packages:

```bash
pip install requests fhir.resources matplotlib
Use Jupyter to open and run the notebook:


jupyter notebook fhirproblems.ipynb
📎 Attribution
This lesson was developed by:

Patrick W. Jamieson, M.D., Technical Product Manager

Russ Leftwich, M.D., Senior Clinical Advisor for Interoperability


📬 Feedback & Contributions
Contributions and feedback are welcome. Please open an issue or pull request on GitHub.


