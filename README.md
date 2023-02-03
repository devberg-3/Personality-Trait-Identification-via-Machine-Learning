
# Personality Trait Identification via Machine Learning

This platform is applicable in various business fields that demand specialist personnel. It will lighten the load of the personnel department responsible for hiring, training, and dismissing employees. The platform will assist in choosing the suitable candidate for a specific job position, thus providing the organization with expert personnel. The administrator can quickly narrow down a candidate based on their personality scores and choose the best fit for a job role.



# Central Theme

The Five Personality Traits, also known as the "Big Five" or the "Five-Factor Model," are a widely researched and commonly used system of personality classification. They consist of five broad dimensions of personality:

## Openness
Reflects imagination, creativity, and appreciation for art and beauty. People high in openness tend to be curious and enjoy exploring new ideas and experiences. They are often open-minded and value novelty and variety
## Conscientiousness
Reflects organization, dependability, and self-discipline. People high in conscientiousness are responsible and hardworking, and they take their obligations seriously. They tend to be reliable, efficient, and goal-oriented.

## Extraversion 
Reflects sociability, energy, and assertiveness. People high in extraversion are outgoing, energetic, and enjoy being around others. They tend to be confident, assertive, and talkative.
## Agreeableness
Reflects trust, cooperation, and empathy. People high in agreeableness are friendly, cooperative, and empathetic. They tend to be good at getting along with others and are often willing to compromise.
## Neuroticism
Reflects emotional instability, anxiety, and moodiness. People high in neuroticism are prone to negative emotions, such as anxiety and worry, and may be more sensitive to stress and life's ups and downs. They tend to be less emotionally stable and more easily distressed.







# Application


These traits are considered to be relatively stable across a person's lifespan and can be measured through various personality assessments and self-report surveys. Understanding the Five Personality Traits can provide insights into an individual's behavior and can be useful in various fields, such as psychology, HR, and marketing.

The system built in this project predicts personality of peoples by using their gender, age, score of openness, conscientiousness, extraversion, agreeableness, neuroticism and experience. It parses all the data from CV/resume and on the result page, it shows all the information from the entered data and uploaded resume. This system uses logistic regression for training the model and pyresparser module for parsing the information from resume which is built using nltk and spaCy module in python. 
# Dependencies of System

•	os

•	pandas

•	numpy

•	tkinter

•	functools

•	pyresparser

•	sklearn

•	nltk

•	scaPy

# Module Functions


Resume parsing specifically refers to the process of extracting relevant information from a job candidate's resume, such as their name, contact information, education, and work experience. PyReParser can be used for resume parsing by defining regex patterns to match the relevant information in the resume and extracting it using PyReParser's API.

By using PyReParser for resume parsing, organizations can automate the process of extracting information from job candidate resumes, saving time and effort compared to manual data entry.


The Natural Language Toolkit (nltk) is a library for the Python programming language that provides support for processing and analyzing human language data. NLTK is designed to make it easy for developers to perform a wide range of natural language processing (NLP) tasks, such as tokenization ,part-of-speech tagging, named entity recognition,etc. NLTK is a powerful tool for NLP and is widely used in academic research and industry for tasks such as text classification, sentiment analysis, machine translation, and more.



Tkinter is a standard Python library for building graphical user interfaces (GUIs). It provides a set of tools and widgets for building desktop applications with a graphical user interface. Tkinter is built on top of the Tcl/Tk GUI toolkit and is designed to be a simple and intuitive way to create GUI applications in Python.


# Working 

The system built in this project predicts personality of peoples by using their gender, age, score of openness, conscientiousness, extraversion, agreeableness, neuroticism and experience. It parses all the data from CV/resume and on the result page, it shows all the information from the entered data and uploaded resume. This system uses logistic regression for training the model and pyresparser module for parsing the information from resume which is built using nltk and spaCy module in python.

### train_model class

It contains two method which train the model and predict the result by giving the various values. train method: It read the dataset for training the model from a csv file and build a model using Logistic Regression. It uses different 7 values for training the model. test method: It predict the personality of a person by passing an array of values that contains gender, age and other 5 personality characteristics.

### main method
We start with creating an object of train_model class and train the model by calling train method of class. Then we initialize a variable with Tk object and design the landing page of system using labels and button. A button with name Predict Personality is designed which calls predict_person¬ method.

### predict_person method
We withdraw the root tkinter window and create a new toplevel window and configure its size and attributes. We label the heading of window followed by various labels and their entries. For selecting of a resume file, user needs to press choose file button which then calls Openfile method that takes an argument of button. In predict_person method, various entries are taken for predicting the personality. Submit button pass all the values to prediction_result.

### openFile_method
It tries to open the directory with default address name and file types and except if file not chosen. After try except block, the method changes the name of choose file button in predict_person method with the base name of file so that user can know about the chosen file.

### prediction_result method
This method firstly closes the previous tkinter window which was used to take the data from user. After this, it calls test method of model object and stores the result returned by method. After this it parse all the information from resume and stores in a variable followed by a try except block which try to delete name and validate mobile number from fetched information from resume. Then it prints all the data submitted by user on console. After this, the method popup a full screen window which shows all the parsed information and predicted personality on GUI window along with the definition of each personality characteristic’s definition.

### check_type method
It converts various strings and numbers into desired format and converts lists and tuples in string.
