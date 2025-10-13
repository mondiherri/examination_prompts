## Compare current claims to previous claims, determine changes and compare for basis in the description
- **Description:**  
These prompts aim to use [Patty](https://chatgpt.com/g/g-67eba45560b08191a2dc76c46d82b4d3-patty) to provide an assessment of the amendments introduced with the latest claims regarding Article 123(2) EPC.
From experience, Patty has sometimes problems with the term *original claims* because it tends to think of them as some claims already provided in the conversation session.
- **Pre-requirements:**  
None!
This prompt can be used without the *"Starting prompt"* (from *"00 - Starting prompt.md"* in this folder.)
- **Documents used:**  
  - **clms-orig.pdf** file containing the **Claims as originally filed**;  
  - **desc.pdf** file containing the **Description as originally filed**;  
  - **clms.txt** file containing the **latest claims**.
  - **Note:**  
    If the claims are in a .pdf or other format (.docx) or the original claims and description are part of an **A1** publication, **change the prompt before submitting!**
- **Caution!**
  - Properly checking amendments is a task at which Patty might struggle. By design LLMs are based on statistical methods for generating text and are prone to summarization and interpretation of text. By contrast, the requirements under **Article 123(2) EPC** are such that an **uninterpreted literal basis** is often necessary.
  - In addition to that, ChatGPT (on which Patty is based) uses software to extract text from PDF documents which might assign different paragraph numbers than those displayed when opening the same PDF document in Adobe Acrobat or some other reader. 

## Only claim 1  
#### Prompt:
    **UserAction: User should upload the documents containing:  
    - the claims as originally filed;  
    - the description as originally filed;  
    - the latest claims on file.**  
    **Note: If the user has not provided all of the required documents, ask the user to upload the documents.**
    **Important: The original claims and description define the application as originally filed for the purpose of the assessment of amendments.**

    - the latest claims on file are in clms.txt.  
    - the claims as originally filed are in clms-orig.pdf.  
    - the description as originally filed is in desc.pdf.  
    1. Check if these documents contain machine readable text. 
    If so:  
    2. Provide a complete comparison of *all* amendments made to the latest claim 1 as compared to claim 1 as originally filed. Amendments can be made by addition, deletion or reordering of wording. 
    3. Indicate if there is a basis in the application as originally filed which directly and unambiguously discloses the identified amendments. First check the claims as originally filed for basis of amendments, then check the description.
    4. Determine if the amendments meet the requirements of Article 123(2) EPC as expressed in the relevant Guidelines.
    
## All claims   
### Identify all amendments   
#### Prompt 1:  
    **UserAction: User should upload the documents containing:  
    - the claims as originally filed;  
    - the description as originally filed;  
    - the latest claims on file.**  
    **Note: If the user has not provided all of the required documents, ask the user to upload the documents.**
    **Important: The original claims and description define the application as originally filed for the purpose of the assessment of amendments.**

    - the latest claims on file are in clms.txt.  
    - the claims as originally filed are in clms-orig.pdf.  
    - the description as originally filed is in desc.pdf.  
    1. Check if these documents contain machine readable text. 
    If so:  
    2. Provide a complete comparison that identifies each amendment in each of the claims in respect of the claims as orifinally filed.
    
### Determine basis and reasoning.   
#### Prompt 2:  
    For each of the identified amendments:
    3. Indicate if there is a basis in the application as originally filed which directly and unambiguously discloses the identified amendments. First check the claims as originally filed for basis of amendments, then check the description.
    4. Explain whether the amendment is allowable or not.
     
  ### Follow up

#### Prompt 3:
    Are there other amendments to claim 1?
    
#### Prompt 4:  
    Are there other amendments made to the rest of the claims?
  
--------------------------------------------

### Formatting the amendments as HTML diff   
Some tools accept pasting text in HTML format.  
The user should open the downloaded HTML and copy the text with the visible amendments as displayed.  
**If you have a long claim, I strongly recommend using some other tool for comparing literal text, because language models are made for analysing and summarizing text. Patty might change a long text, without the user noticing!**

#### Prompt:   
    1. Can you display these amendments in a diff format in html, starting from the literal text of claim 1 as originally filed?   
    Added words should be underlined. 
    Deleted words should be in strikethrough.
    
    2. export the above as a downloadable HMTL.















