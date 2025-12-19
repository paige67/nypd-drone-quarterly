# nypd-drone-quarterly
NYPD's quarterly "Unmanned Aircraft Systems (UAS) Operations Report"
I wanted to build a scraper that would allow me to easily pull down NYPD's quarterly data about drone flights -- specifically to track the growth of their "drone as a first responder" program. 

Data about NYPD drone launches is supposed to be updated quarterly in a machine-readable format here (https://www.nyc.gov/site/nypd/stats/reports-analysis/uas-drones.page). If you click on the link for each quarter, an excel file will automatically download. Even though this is easy enough, it is helpful to programtically scape the website to learn the technique and to stay organized with the files. 

Most of the scraping was easy enough as the files were well named and organized (Base_url + {year}-{quarter}) but then there were a handful of snags. Inside the files themselves, the NYPD was skipping rows in different ways, so I had to use a function to find the data inside the excel file. Then, when I went to update this data I found the NYPD is no longer using their clean naming convention and instead named their files "_2q_report" and "_3q_report_final" this year, which undermines the usefulness of my scraper long term. Both of these fixes were slightly beyond my scraping capablities and I used Google's Gemini AI coding tool for assistance. 

The end result is also a slightly messy data frame but the data I actually need for research is clear: the NYPD's "drone as first responder" program is the majority of all drone flights in the city and has continued to grown. 

Brooklyn and The Bronx have had 5,600 and 4,600 DFR flights in the year and a half -- making up about 85 percent of each of the total drone flights that have taken place over the past six years in the boroughs. In the city over all, despite being a new program, it now accounts for 70 percent of historic drone flights, over 11,000 launches. 

The program allows officers to launch drones remotely from police precincts and has faced criticism from anti-surveillance advocates and tech watchdogs, as the drones have the potential to be fully automonous and reportedly can connect to the NYPD's domain awareness system. 
