
#######PDF Resume Parser
This Python script extracts the following sections from a PDF resume:

-Tools: Computer skills and software competencies
-Education: Academic degrees, certificates, and courses
-Work Experience: Employment history, job titles, and responsibilities
-Langue: Language skills and proficiency levels
-Activities: Professional affiliations, volunteer work, and extracurricular activities


####How to Use

Clone or download the repository to your local machine
Install the dependencies using pip install
Replace the cv.pdf file in the root directory with your own PDF resume (make sure the file name is the same)


####How It Works


The script uses a combination of regular expressions and natural language processing (NLP) techniques to extract the relevant sections from the PDF resume.
First, the script reads the entire PDF document using the fitz library and iterates over each page. For each page, it normalizes the text by removing diacritics, converting to lowercase, and ignoring non-ASCII characters. This is done to standardize the text and make it easier to search and match with regular expressions.
Next, the script uses a series of if statements to search for specific keywords in the normalized text. For example, if the keyword "informatiques" is found in the text, the script assumes that the following section contains information about computer skills and software competencies. Similarly, if the keyword "formations" is found, the script assumes that the following section contains information about academic degrees and courses.
Once a keyword is found, the script extracts the relevant text using string slicing and stores it in a variable. The extracted text is then cleaned and processed using NLP techniques such as tokenization, part-of-speech tagging, and named entity recognition. This allows the script to identify specific types of information within the text, such as job titles, company names, and dates of employment.
Finally, the script stores the extracted information in a pandas dataframe and saves it to a CSV file.
