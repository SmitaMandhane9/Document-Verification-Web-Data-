# Document-Verification (Web Data)


# Project Title

Document Verification Check Results for Customer Due Diligence in Banking 

# Problem Statement

In the banking industry, ensuring the authenticity and completeness of customer documents is a critical part of Customer Due Diligence (CDD) and regulatory compliance. However, banks often struggle with high volumes of unstructured or incomplete documentation, leading to delays in onboarding, compliance risks, and potential financial losses. This project aims to analyze and visualize the outcomes of document verification checks to identify patterns, highlight common failure points, and support process optimization for improved customer verification efficiency.

# Dataset Details

**1. Dataset Duration:**

      May 23 – May 31 (~2 weeks)
      June 2017 – October 2017

**2. Clearance Rate Definition:**
   
      The clearance rate is defined as the number of customers who pass the document verification process (i.e., records that return “clear” as output),              divided by the total number of customers who attempt the process.

      Clearance Rate = Clear Output Count / Total Attempt Users

**3. Key Columns and Their Descriptions**

      a. visual_authenticity	-> Asserts whether visual, non-textual elements are correct given the type of document.
      
      b. image_integrity ->	Asserts whether the document was of sufficient quality to verify.
      
      c. data_validation -> Asserts whether algorithmically validatable elements are correct (e.g., MRZ lines and document numbers).
      
      d. data_consistency ->	Asserts whether data represented in multiple places on the document is consistent (e.g., MRZ lines vs. OCR text).
      
      e. data_comparison ->	Asserts whether data on the document is consistent with data provided by the applicant (via application form or API).
      
      f. police_record ->	Asserts whether the document has been identified as lost, stolen, or otherwise compromised.
      
      g. compromised_document -> Asserts whether the image of the document has been found in the internal database of compromised documents.

**4. Sub-result Field Definitions**

      ❌ Rejected – The check could not be processed due to poor quality or unsupported documents.
      
      ⚠️ Suspected – The document is suspected to be fraudulent.
      
      🟡 Caution – Other checks failed, but not necessarily indicating fraud (e.g., mismatched applicant names).

# Findings

1. 23% of total users have attempted the verification process multiple times, indicating potential issues with document quality, user understanding or system usability.
![image](https://github.com/user-attachments/assets/d11f3895-0de0-4ed9-b97e-fbc324d83f98)


<img width="983" alt="image" src="https://github.com/user-attachments/assets/e81b077a-2784-4c3a-b41d-9857a9aebb53" />

<img width="643" alt="image" src="https://github.com/user-attachments/assets/12c76b85-e461-468f-af69-ae6d97c588a4" />

