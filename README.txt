# Import request & BeautifulSoup from bs4
import requests as r
from bs4 import BeautifulSoup

# Sending request to server(apna page)
response = r.get("https://thesujaljaiswal.github.io/exams.github.io/")

# Create Soup object to search(response.text as input)
soup = BeautifulSoup(response.text, 'html.parser')

# Print results
print(soup.find("pre", id="threadarmstrong").text)