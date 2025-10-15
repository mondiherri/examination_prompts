## Unity of invention (Article (82 EPC)
**Description:**  
This workflow has not yet been tested in detail.

### Read the claims   
#### Prompt:  
    **UserAction: User should upload a document containing the claims.**  
    **Note: if the user has not provided any document, ask the user to upload the claims.**   
     
    Me and you are examining case EP12345678. 
    The latest claims are in clms.pdf (or clms.txt)  
    Check if the file contains machine readable text. 
    If so:
    - How many independent claims are there and what are their categories?

### Recall the relevant Guidelines:   
#### Prompt:  
    **Note: The user should specify a list of sections from the Guidelines.**  
    
    2. In detail, explain what are the requirements expressed in the following Guidelines regarding clarity of the claims.  
    Do not apply these to the claims yet.  
    – F-V, 2   
    – F-V, 2.1   
    – F-V, 2.2   
    – F-V, 3
    - F-V, 3.3.1

### (Alternative) Unity a priori without comparison to prior art
#### Prompt:  
    3. How do the principles from the previously mentioned Guidelines apply to the claims?

### (Alternative) Unity after comparison of claims to prior art 
#### Prompt:
    **UserAction: User should upload a document containing the prior art.**  
    **Note: if the user has not provided any prior art document, ask the user to upload the necessary document.**  
     
    D1, D1.pdf, is a prior art document.   
    Check if the uploaded document contains machine readable text.  
    If so:  
    3. How do the principles from the previously mentioned Guidelines apply to the claims in the presence of this prior art?




