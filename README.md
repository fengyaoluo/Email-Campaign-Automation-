

## “One-Month Free Storage” Email Campaign Project
 
In order to increase the number of online reservations for storage rentals, we launched an emailcampaign to send emails to truck and trailer customers conveying that they are qualified to get a one-month free rental at a nearby U-Haul storage center. We picked nearly 200 locations in the U.S. andCanada and updated the lists regularly based on their occupancy rate or seasonality such asschool/holiday season. However, this task required 2 hours daily to complete. Thus, I wrote a python
code to automate this process, thereby freeing up my coworker’s time. 

The process was as follows:
 
* Use python to automate the formatting process. 

Before I created the automation for my coworker, he had to format the data daily before he sent out thecampaign emails through Dotdigital. It involved pulling the customer list from Uhaul.net Report Center, downloading the list, formatting it by removing duplicates, capitalizing the first character of customers’ first and last name, and using vlookup function to add our storage location name, address, phone, URL,etc. It usually took him 1.5-2 hours every morning to finish the whole process. Afterwards, a digital specialist would manually concatenate UTM tracking codes to URLs in Excel. My Python automation accomplished all those functions automatically without my coworker having to spend any time. Please refer to **the attachments** to see my actual automation python code. 

The functions written can be summarized as: 

set up the template as CSV files (Separated by In-Town and One-Way) < use PANDA toread the file (pd.read_csv) < proper case first name & Last name (str.title) < remove duplicates and invalidemail address (apply(lambda x: validate_email(x)) < create City, ST for vlookup (df.merge) < separate bydifferent lists < add UTM tracking code < export the list to folders. 
