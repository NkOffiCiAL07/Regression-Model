# HELPER FUNCTIONS
## CSV
To read a csv file and convert into numpy array, you can use genfromtxt of the numpy package.
For Example:
```
train_data = np.genfromtxt(train_X_file_path, dtype=np.float64, delimiter=',', skip_header=1)
```
You can use the python csv module for writing data to csv files.
Refer to https://docs.python.org/2/library/csv.html.
For Example:
```
with open('sample_data.csv', 'w') as csv_file:
	writer = csv.writer(csv_file)
    writer.writerows(data)
```
## PICKLE
You can use the pickle library (Reference: https://www.geeksforgeeks.org/saving-a-machine-learning-model/)
1. To store the training classifier into the model file.
For example:
	```
	pickle.dump(model, open('model_file.sav', 'wb'))
	```
2. To load the model from model file.
For example:
	```
	model = pickle.load(open('./model_file.sav', 'rb'))
	```