# Everyday Hero#

We heard that the rate of people gone missing have risen lately and we wanted to do something about it. Thinking about what we could do to help, we also remembered about the multiple occasions when, going back home at night or walking around certain neighborhoods we would have appreciated someone to make us feel safe. That's when the idea came to us. Why can't we have an app that provides us that kind of safety? Why can't people around us know that we are in a struggle and help? And why can't we do the same to make other people's lives a little better? Why can't we all be heroes for each other in small ways?

## What it is going to do#
Everyday Hero is an Android app with an intuitive interface that protects you in several levels.

The first situation would be when you are in a situation in which you would need someone to walk by your side and make you feel safer. With this app, you can achieve that in just one click.

By using the "I'm scared!" button, a message is immediately sent to all the users around your perimetre within your location and the option of chatting with them is also available.

Secondly, if you are in a real danger situation, there's a second button that gives you the option to ask for help to the authorities. People around you are also alerted about your situation through a notification and, in order to draw everyone's attention, an alarm will start to ring from the victim's phone.

Finally, the application gives the user the chance to make a difference by finding people in danger around them and dedicating some time to improve their day.

## Working with the server#
The server is up and ready to receive and hand out information. In order to use it, the library **requests** for Phython servers is strongly recommened. The main commands that one might use are:

### Post request
```python
r = requests.post('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users', params = user_data, headers = headers)
```

'Headers' must define the Content's type:
```python
headers = {'Content-Type': 'application/json'}
```

and user's data format should be something such as:
```python
{'Longitude': '10', 'Latitude': '12.2', 'id': 2}
```

### Get request
```python
r = requests.get('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users' + '1')
```

### Put request
```python
r = requests.put('http://ec2-35-167-168-2.us-west-2.compute.amazonaws.com:5000/api/users' + '1', params = user_data, headers = headers)
```

In every case, 'r' is going to be an object containing some information that can be treated either in the server or using any external application. 
