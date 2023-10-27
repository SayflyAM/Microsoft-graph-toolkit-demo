# Microsoft-graph-toolkit-demo
you can use Python to make calls to the Microsoft Graph API. Microsoft provides the Microsoft Graph API 
Register your Application in the microsoft Azure portal including the client ID and client secret
you need to install python library called "requests" which allows you to make HTTP requests
open your terminal and paste "pip install requests"

Here's a simple example of making a GET request to retrieve a user's profile using the Microsoft Graph API in Python:
---------------------------------------------------------------
import requests

url = "https://graph.microsoft.com/v1.0/me"
headers = {
    "Authorization": "Bearer YOUR_ACCESS_TOKEN"
}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    data = response.json()
    print("User Display Name:", data["displayName"])
else:
    print("Error:", response.status_code, response.text)
----------------------------------------------------------------


