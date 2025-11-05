# Analysing Inventive Step

### Simple analysis based on previously determined closest prior art and further document.  

- **Description:**  
  This prompt is intended to use  [Patty](https://chatgpt.com/g/g-67eba45560b08191a2dc76c46d82b4d3-patty) for cases where the closest prior art and another prior art document have already been identified. Patty is used to analyse the documents and generate the text of the analysis.  
It has worked in some cases, but the result might not be reliable in other cases. Especially the length of the claim or the lenght of the prior art documents might make the prompt not reliable.
- **Documents used:**
  - .pdf or .txt file containing the **Claims** in machine readable form.
  - **At least one prior art** document in .pdf format, for ease of reference name them **D1.pdf**, **D2.pdf**, etc...
     
#### Prompt:
    **UserAction: User should upload a document containing the claims and at least a document containing the prior art.**  
    **Note: if the user has not provided the documents, ask the user to upload the claims or the prior art.**
	
    You are a european patent examiner examining the case EP00000012. 
	The latest claims are in clms.txt. 
	The closest prior art is in D1.pdf. 
	D2.pdf is a further prior art document. 
	Step by step: 
	- Assess novelty of claim 1 over D1.pdf. 
	- Assess inventive step of claim 1 over a combination of D1.pdf and D2.pdf.

### Complex workflow for assessing inventive step without a priori in-depth knowledge of documents.
- **Description:**  
This prompt sequence is intended to use [Patty](https://chatgpt.com/g/g-67eba45560b08191a2dc76c46d82b4d3-patty) to inventive step of an independent claim according to the Guidelines.  
No assessment of technical character is involved by this claim, so do not expect Patty to deal with technical character!
- **Pre-requirements:**  
None!  
This sequence incorporates the *"Starting prompt"*.  
Skip the Prompt 1. if you have already provided the claims to Patty.
- **Documents used:**
  - .pdf or .txt file containing the **Claims** in machine readable form.
  - .pdf file containing the **Description** in machine readable form.
  - **At least one prior art** document in .pdf format, for ease of reference name them **D1.pdf**, **D2.pdf**, etc... 
	
#### Prompt 1:  
The text of the claims is pasted in the textbox by  the user.   
    **UserAction: User should paste the text of the claims.**
    **Note: if the user has not provided any claim text, ask the user to paste the claims in the textbox.**  

    Me and you are examining case EP0000001.  
    The literal text of claim 1 is:
    
    > User, paste literal text of claim!

##### Alternative Prompt 1:
The claims are provided as document.  

    **UserAction: User should upload a document containing the claims.**
    **Note: if the user has not provided any document, ask the user to upload the claims.**
    Me and you are examining case EP0000001. 
    The latest claims are in:
    - clms.pdf
	  - clms.txt
     
    Check if the file contains machine readable text. 
	  If so:
	  1. Prepare a FFTP-style breakdown of the features of claim 1,  
	  presenting the Features,  
    the function(s) they achieve,  
    the technical effect(s) they bring about,  
    and the resulting problem(s) solved thereby.

### (Optional) Interpret the claim features in the light of the description:  

#### Prompt 1.1:  
     **UserAction: User should upload a document containing the description.**  
	 **Note: if the user has not provided any document, ask the user to upload the description.**   
	 
	 The description can be found in :
	 - desc.pdf 
	 - a1.pdf, which is the original A1 publication.
	 
	 Check if the file contains machine readable text.  
     If so:  
	 1.1. Verify if the description provides more details regarding the claimed aspects.
	 1.2. Reassess the feature breakdown of claim 1 in light of the disclosure of the description corresponding to each individual feature of the claim.


#### Prompt 2: 
Make a first assessment of inventive step, that you can refine later.  

    **UserAction: User should upload a document containing the prior art.**  
    **Note: if the user has not provided any document, ask the user to upload the prior art document.**  
     
    2. make a full inventive step assessment of claim 1 over the provided prior art documents.

#### Conservative prompt 2:  
    2. Assess inventive step  over the prior art.  
	Be conservative, if an effect is not derivable from the claim features alone, then it is not there.

### Review and Reformat the feature mapping
#### Prompt 3:      
Reformat the feature mapping! Change the example given below to your style.

    - provide a feature mapping of the literal text of claim 1 features to corresponding text passages or paragraphs of D1, disclosing the corresponding claim features.
    - use the following format as an example for the feature mapping:
     *Example*:
     F1) literal text of feature
     (see D1, passage 1, passage 2;
     explanation of disclosure of D1)
     F2) literal text of feature
     (not disclosed in D1) **If a feature is not disclosed, indicate it like this**
     F3) literal text of feature
     (see D1, passage 3; passage 4)
     F4) ...

### Refine the inventive step assessment  
A more condensed format for a **positive** inventive step reasoning.  

#### Prompt 4:  
    - list again the distinguishing features of claim 1 over the closest prior art you selected.   
    - explain the technical effects of the distinguishing features.   
    - formulate an objective technical problem solved by these features.   
    - explain why the distinguishing features solve the objective technical problem.   

### Review and check for arguments for the contrary conclusion. 
**Use one of these options.**  
#### Prompt 5:  
    Could it be argued that the claim does involve an inventive step?

    
#### Alternative prompt 5:
    Could it be argued that the claim does NOT involve an inventive step?  

	
### Review arguments  
### Prompt 6.1:  
Arguments from the applicant  

    **UserAction: User should upload a document containing the arguments.**
    **Note: if the user has not provided any document, ask the user to upload the arguments.**    
    The arguments of the applicant are in the file:  
	- args.pdf    
    Check if the file contains machine readable text:  
    If so:  
    - summarize each of their arguments on inventive step.  
    - draft a response to each of their arguments.  

### Prompt 6.2:  
Assessment from the examiner  

    **UserAction: User should upload a document containing the assessment of the examiner.**  
    **Note: if the user has not provided any document, ask the user to upload the assessment of the examiner.**    
    The assessment of the examiner is in the file:  
	- comm.pdf  
    Check if the file contains machine readable text:  
    If so:  
    - summarize each of their arguments on inventive step.  
    - draft a response to each of their arguments.  

	
