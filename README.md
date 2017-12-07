### Sprint 2: Python Webscraping on a Virtual Machine

11/28/17 - 12/7/2017:

**Author:** Olina Cavedoni

__*Project Description:*__
The objective of this project was to create a virtual machine "Droplet" with a Jupyter Notebook, and then use python to scrape data off of a website to retrieve SP500 data. 

__*Steps:*__

Digital Ocean
- Open link to Digital Ocean: http://https://cloud.digitalocean.com/droplets?i=d4ca35
- Click on "Create" and then click on "Droplet"
- Choose your image type (Ubuntu)
- Choose your cloud size (Standard, 512 MB 1CPU, 20 GB SSD Disk, 1000GB Transfer, $5/mo)
- Choose your data center (SFO 1)
- Create and add your SSH key
- Set up Jupyter Notebook into your Droplet

Python
- Put your virtual machine Droplet's IP Address into your web browser: 192.241.209.169
- Click "New" and "Python 3" to open a Python file
- Write the following code
      *import pandas as pd*
      - Imports pandas, can be accessed using shortened name "pd"

      *data = pd.read_html('https://en.wikipedia.org/wiki/List_of_S%26P_500_companies')*
      - An easy pandas code that allows you to declare a website to scrape

      *table = data[0]
      table.head()*
      - Creates a table, and displays the first 5 rows

      *sliced_table = table[1:]
      header = table.iloc[0]*
      - Removes the first row and then creates a header

      *corrected_table = sliced_table.rename(columns=header)
      corrected_table*
      - Declares a new table that combines the original table with the sliced first row as a header, then displays the new table

    Done!

__*Notable Observations:*__
Jupyter Notebook is great. I don't know how I'd use my Digital Ocean Droplet server without it.

__*Next Steps:*__
Create tables and "Join" them.
