## Steps Taken to work on the puzzle 
1. Intially the Nginx port mapping is worng, it has to be 8080:80
2. If, we fix the above and run the code we get 502 bad-gateway, because the official port of Flask app is 5000 not 5001. Hence we need to make necessary changes in the Dockerfile and the /conf.d/flaskapp.conf file
3. Make sure that we fix the port in the app.py file, and follow the standard for app.run(host='0.0.0.0',port=5000) not just app.run(host='0.0.0.0')
Lastly, in method success() in the file app.py, we receive a list of object of class Items. We have to iterate through the list to extract the data from it and return to the user.
