Here are the documents that serve as the basis for RAG for Patty.

The files case_law_2025.md and Guidelines_2025.md are cleaned extractions from the pdf files using the python library pymuPDF.

I first extracted the text content from the pdf files, then manually cleaned the text files and generated the md formatting, which is basically just formatting certain headers.

**After experimenting with the markdown files for some days I realized that the extraction is not complete and that ChatGPT does not completely parse the md file. Therefore I have reverted to using the original PDF documents as input to the knowledge base.**
