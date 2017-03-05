# HackUpcWinter

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
