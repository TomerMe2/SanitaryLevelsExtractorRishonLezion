# Extraction of Sanitary Levels From PDFs Published By Rishon Lezion Municipality
## Background
Open data is important. Especially when it comes to the health of the people. <br/>
As a citizen of Rishon Lezion I wanted to know if there are locations that I eat in that have poor sanitary. <br/>

"התנועה לחופש המידע" has requested Rishon Lezion municipality to publish the sanitary checkups that they have done in some food related businesses. <br/>
Rishon Lezion municipality published this data, but in a way that will help them to hide the actual data. <br/>
Each checkup for a single resturant has a single PDF. Almost all the PDFs has file names that don't allow you to know what business is the topic of this checkup. All the PDFs are scans of papers, so they are practically images and not texts. <br/>

"התנועה לחופש המידע" made a freedom of information request (בקשה לחופש מידע) to Rishon Lezion municipality in order to receive this data. <br/>
More info can be found here: https://www.meida.org.il/?p=11611 <br/>

The municipality published this data in a ZIP file that contains a lot of PDFs with super generic names, like: 'דוח ביקורת (18)'. <br/>
Most of the times, you couldn't tell the resturant name from the file name. These PDFs are scans of papers, so they are practically images and not texts. <br/>


## Technological Solution
I'm using Tesseract OCR with some search heuristics to locate the important lines and then I'm extracting the important data from these lines. <br/>
Using Levenshtein distance was cruicial to the success of the search heuristics because the OCR isn't perfect and it might detect texts that are off by a small amount of characters compared to the original text. For example, the OCR predicts 'ט' instead of 'ם' a lot of time.
I made this code to create an excel file to search for locations and to look on the data in an organized way. <br/>

The xlsx file that this notebook outputs (with some changes) can be found here: <br/>
https://docs.google.com/spreadsheets/d/1xXSeL0NzFHiJ-lNoXwo6rvfhVkyRTw7lyOBnxiTU4oA/edit#gid=1376681010
