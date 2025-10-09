# Prompting for analysing patents and patent applications

## Patent documents and practitioners
A patent application or publication, is a formal document which has certain legally defined parts. 
Usually it contains: 
* a set of claims
* a description
* a set of drawing sheets

The content of these parts is regulated by law and should fulfil certain legal criteria defined by law (e.g. EPC), regulations (e.g. Guidelines) or case law.
These documents contain highly specialized subject matter which most often requires a long formal training to understand, such as a scientific Master's degree or PhD.
In order to understand the legal framework, further training is needed on top of the Master or PhD.
Examiners spend many years learning on-the-job at the EPO while Patent Attorneys have to pass the [EQE] (https://en.wikipedia.org/wiki/Representation_before_the_European_Patent_Office#European_qualifying_examination).
The EQE is an a four-parts exam which cumulatively lasts 18,5 hours. Most candidates sit the different parts of the EQE over several years.

## Analysing a patent document
Analysing a patent related document (i.e. an application or publication) consists in checking to what extent the document fulfills the requirements set by the law, regulations and the case law.
This is usually a high level intellectual work, which requires a lot of preparation (see above), quite some time and is best done after a good nights' sleep.

The prompts in this repository are an attempt to use the possibilities offered by modern GenAI models to facilitate the analysis of such highly complex information in the presence of two constantly moving targets: 
* technical progress
* legal frameworks and practice

Usually the analysis of patent documents involves a number of phases:
1 Analysing and understanding the technical content (in the sense of [techne](https://en.wikipedia.org/wiki/Techne)) of the patent document (application or publication).
2 Recalling the law, regulations or case law that might apply.
3 Checking if the patent document fulfils applying legal requirements (e.g. clarity, unity of invention, amendments, sufficiency of disclosure, exception or exclusion from patentability)
4 Comparing the content of the patent documents to the available prior art (e.g. for novelty and inventive step) 
5 Forming an opinion, including deciding what are the most important problems that a patent document might have and disregarding minor problems.
6 Consider any previous arguments made by an examiner or applicant and form an opinion on these
7 Drafting a text which reflects this opinion in an understandable manner for anyone who might read it (usually an examiner or the representative of an applicant).

## GenAI
Modern LLMs have made great progress in some of the above tasks faced by anyone working with patents. 
They can analyse and understand technical and legal content. They can reason about it and can draft a text reflecting their "analysis".

The 7 big steps I use when working with LLMs are:

1 Analysing and understanding the technical content, in this order.
 * upload the claims to the LLM and ask it to summarize (as pdf or txt file)
 * upload the description to the LLM and ask it to summarize (as pdf or txt file)
 * Verify that the response makes sense!
2 Recalling the law
 * One can ask the LLM to do an upfront analysis of salient problems or just remind themselves of the important legal framework for the given case.
 * Retrieval augmented generation is used to "remind" the LLM of the details of the important legal aspects.
 * Verify that the response makes sense!
3 Checking if the claims and description fulfil the legal requirements that apply without regard to the prior art
 * Ask the LLM to apply any case-relevant legal requirements on clarity, sufficiency of disclosure, unity of invention, amendments, exception or exclusion from patentability.
 * Verify that the response makes sense!
 * Ask for arguments supporting the contrary point of view. 
 * Verify that the response makes sense!
4 Comparing the technical content of the claims/description to the available prior art
 * In a loop (not more than 5 times for a given session. If needed start another session as the LLMs might get confused.):
   - upload a prior art document to the LLM and ask it to compare the claim to the prior art document
   - Verify that the comparison makes sense!
5 Ask the LLM to choose a closest prior art and assess novelty and inventive step.
 * Verify that the response makes sense!
6 Ask the LLM to analyse previously made arguments on the case
  * upload the previous arguments (as pdf or txt file)
  * ask the LLM to summarize the arguments and respond
  * Verify that the response makes sense!
7 Ask the LLM to draft a letter containing the result of all of the above
  * Verify that the response makes sense!

## Conclusions
The idea in this work is to provide prompts which reflect the above process of:
- understanding the technical and legal aspects
- exploring points of view to form an opinion
- drafting a human-understandable text reflecting the opinion.
  
Often, the process needs to be reiterated, because each of these steps may be incomplete.

This is a lot of work. But an LLM can simulate reasoning and generate text much faster than a human being, which hopefully should allow the person to do something more personally or socially valuable than typing with their time.
Once one gets some experience with the process, one develops a better intuition of how to work with LLMs in such a complex field as patents. 

## Don't embarrass yourself!
Each of the steps included herein need human verification, because even if arguments are generated by an LLM, in a legal process such as patent prosecution these arguments are always brought to the other side by a human being ;) .

It is really cringe when someone reads your unchecked GenAI text! 

## Disclaimer!
If you are thinking that by using LLM-generated text, you can overwhelm the other party with text, keep in mind that step 6 is also performed at the speed of billions of transistors. 
At such speeds, the difference between analysing two hundred pages or two paragraphs of arguments, tends to be negligible.
