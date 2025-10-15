## Prompt for starting analysis of a set of claims.
**Purpose:**  
Make the model *"understand"* the claim features.

#### Prompt 1:  

    **UserAction: User should upload a document containing the claims.**
    **Note: if the user has not provided any document, ask the user to upload the claims.**
	 
    Me and you are examining case EP0000001. 
    The latest claims are in:
	- clms.pdf
	- clms.txt
	
	Check if the file contains machine readable text. 
	If so:
	1. Prepare a FFTP-style breakdown of the features of claim 1,  
	presenting in a table, the Features,  
	the function(s) they achieve,  
	the technical effect(s) they bring about,  
	and the resulting problem(s) solved thereby.

### (Optional) Interpret the claim features in the light of the description:  

#### Prompt 2:  
    **UserAction: User should upload a document containing the description.**  
	  **Note: if the user has not provided any document, ask the user to upload the description.**   
	 
	  The description can be found in :
	  - desc.pdf 
	  - a1.pdf, which is the original A1 publication.
	 
	  Check if the file contains machine readable text.  
      If so:  
	  2.1. Verify if the description provides more details regarding the claimed aspects.
	  2.2. Reassess the feature breakdown of claim 1 in light of the disclosure of the description corresponding to each individual feature of the claim.
  

### Summarize the claim in plain language:  

#### Prompt 3:  
    3. Summarize the subject matter of the claim in plain language that a person skilled in the art can understand easily.

### Examine sufficiency of disclosure

#### Prompt 4:  
    4. For each claimed aspect, explain whether the description discloses the subject matter in sufficient detail for the skilled person to be able to carry out the claimed aspect.

#### Prompt 5:   
    5. Identify any features which might not be disclosed in sufficient detail for the skilled person to be able to carry them out?






