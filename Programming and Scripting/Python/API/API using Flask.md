
# Get Request
```python
from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/users')
def home():
    users = {
        "users": [
            {
                "name": "Mark",
                "age": 28
            },
            {
                "name": "Vince",
                "age": 35
            }
        ]
    }
    return jsonify(users), 200

if __name__ == '__main__':
    app.run()

```



# Get Request Specific
```python
from flask import Flask, jsonify, request

app = Flask(__name__)

usersData = {
    "users": [
        {
            "id": 1,
            "name": "Mark",
            "age": 28
        },
        {
            "id": 2,
            "name": "Vince",
            "age": 35
        },
        {
            "id": 3,
            "name": "Lumen",
            "age": 30
        }
    ]
}


usersData['users'].append(newUser)
print(usersData)

@app.route('/users')
def users():
    global usersData
    print(usersData)
    return jsonify(usersData), 200


@app.route('/users/<userId>')
def specific_user(userId: int):
    global usersData
    try:
        userId = int(userId)
    except:
        return jsonify({"Response":"There was an error processing your request, check the user id."}), 400

    for user in usersData['users']:
        if user['id'] == userId:
            return jsonify(user), 200
    #return "<h1>User was not found</h1>", 404
    return jsonify({"Response":"User was not found"}), 404


if __name__ == '__main__':
    app.run()

```



# POST Request
```python
from flask import Flask, jsonify, request

app = Flask(__name__)

usersData = {
    "users": [
        {
            "id": 1,
            "name": "Mark",
            "age": 28
        },
        {
            "id": 2,
            "name": "Vince",
            "age": 35
        },
        {
            "id": 3,
            "name": "Lumen",
            "age": 30
        }
    ]
}

@app.route('/users', methods=['POST'])
def create_users():
    global usersData
    newData = request.get_json()
    usersData['users'].append(newData)
    print(newData)
    return jsonify(usersData), 200


if __name__ == '__main__':
    app.run()
```




# DELETE Request
```python

from flask import Flask, jsonify, request

app = Flask(__name__)

usersData = {
    "users": [
        {
            "id": 1,
            "name": "Mark",
            "age": 28
        },
        {
            "id": 2,
            "name": "Vince",
            "age": 35
        },
        {
            "id": 3,
            "name": "Lumen",
            "age": 30
        }
    ]
}


@app.route('/users/<userId>', methods=['DELETE'])
def delete_user(userId):
    global usersData
    try:
        userId = int(userId)
    except:
        return jsonify({"Response":"There was an error processing your request, check the user id."}), 400
    for user in usersData['users']:
        if user['id'] == userId:
            usersData['users'].remove(user)
            return jsonify({'Response': f'User {userId} was successfully deleted.'}), 200

    return jsonify({"Response":"User was not found"}), 404




if __name__ == '__main__':
    app.run()
```












