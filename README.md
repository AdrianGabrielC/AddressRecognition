A detailed explanation can be found in Doc.pdf in this repository!

1. Problem. I chose to solve the Challenge #1 Address Extraction which implies writing a program that extracts all valid addresses that are found on a list of company websites in the following format: country, region, city, postcode, road and road numbers.

2. Reasoning. First, I decided to use entity recognition to identify addresses in a string containing the contents of a website. Secondly, the reasoning I used is divided in two phases: in the first phase I extract the full address from the string which contains the content of a website and in the second phase I extract the street number, street name, city, region, and ZIP code from a string which contains a full address (obtained in the first phase). 
The reason why I decided not to extract the street number, street name, city, region, and ZIP code directly from the website is that it is possible that a street name or city appears in a website in a different context that its address, resulting in the identification of multiple cities in a single webpage, case in which we cannot say which is part of the address.
I trained two models, one for recognizing the address in a string containing the content of a website, and one for recognizing the street number, street name, city, region, and ZIP in an address string. 

3. Tools used. I used Python with spaCy  (plus some additional tools like beautifulsoup for web scraping, openpyxl to work with .xlsx files) to solve this task. 

4. Results. Out of ~2500 websites (which some worked some didn’t and some contained addresses, and some didn’t) I obtained 509 addresses out of which, 260 are complete (meaning that they have street number, street name, city, region and ZIP) and 249 are incomplete (meaning that either street number or street name or city or region is missing).

A detailed explanation can be found in Doc.pdf in this repository!
