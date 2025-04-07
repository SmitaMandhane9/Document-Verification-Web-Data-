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

1.  23% of total users have attempted the verification process multiple times, indicating potential issues with document quality, user understanding or system usability.

      <img width="241" alt="image" src="https://github.com/user-attachments/assets/b5ed0a8d-cdd2-4ea2-aa63-83a4791330e0" />

      <img width="145" alt="image" src="https://github.com/user-attachments/assets/69ab18d5-4e6f-479b-80fe-974835a8313d" />

2.  As the number of user attempts increases, we observe a decrease in the clearance rate within the dataset. Please note that, for this analysis, only weekly data is available for May. Therefore, the graph below displays data from June to October to understand the impact more accurately

       <img width="375" alt="image" src="https://github.com/user-attachments/assets/8c20233d-d5bc-41b7-a7a3-c2ea086f9171" />

3.  If we look into “Consider” result, we observe a higher rejection rate at the overall level

      <img width="324" alt="image" src="https://github.com/user-attachments/assets/1df8b6d6-223b-40a4-8ee1-855ff1bb23af" />

4.  Upon further analysis, the primary reasons for failure appear to be as follows
   
      <img width="547" alt="image" src="https://github.com/user-attachments/assets/fafb8d11-1da5-4a01-bdf7-f7f416ffae6e" />

      Analysis confirmed that the majority of cases were not considered further due to issues related to image integrity, such as the quality of submitted            images and conclusive document quality.

5.  The national identity card is the most commonly used document for user verification.

      <img width="383" alt="image" src="https://github.com/user-attachments/assets/501166d1-3b6f-411f-a73c-23b72107cb06" />

      <img width="172" alt="image" src="https://github.com/user-attachments/assets/16fcaa55-491c-4540-a080-57cb8900b362" />

6.  Below chart shows the bottom 10 countries with the lowest clearance rates.

      <img width="183" alt="image" src="https://github.com/user-attachments/assets/15185865-2e28-4d9f-a8d9-cf5cc0b36b29" />


# Action items

      - Provide better instructions to users on how to submit clear, high-quality images
      - Make the system easier to use to reduce no. of repeat attempts
      - Improve the verification process to handle document better for country who has low clearance rate















