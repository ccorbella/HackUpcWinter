# Working with the server#
The server is up and ready to receive and hand out information. In order to use it, the library **requests** for Phython servers is strongly recommened. The main commands that one might use are:

## Post request
'''python
r = requests.post('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users', params = user_data, headers = headers)
'''

'Headers' must define the Content's type:
'''python
headers = {'Content-Type': 'application/json'}
'''

and user's data format should be something such as:
'''python
{'Longitude': '10', 'Latitude': '12.2', 'id': 2}
'''

## Post get
'''python
r = requests.get('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users', params = user_data, headers = headers)
'''

## Post put
'''python
r = requests.put('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users', params = user_data, headers = headers)
'''

In any case, 'r' is going to be an object containing some information that can be treated either in the server or using any external application. 
