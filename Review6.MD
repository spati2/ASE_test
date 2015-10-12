[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner1.png">](https://github.com/txt/mase/blob/master/README.md)   
[At a glance...](https://github.com/txt/mase/blob/master/OVERVIEW.md) |
[Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) |
[Models](https://github.com/txt/mase/blob/master/MODELS.md) |
[Code](https://github.com/txt/mase/tree/master/src) |
[Lecturer](http://menzies.us) 


# Review6: Dr. Dam's Talk

+ What are predictive models?
  * Predictive modeling is a process to create a statistical model of future behavior. Predictive analytics is the area of data mining concerned with forecasting probabilities and trends. 
+ What are rule based models?
  * Rule-based modeling is a modeling approach that uses a set of rules that indirectly specifies a mathematical model.
+ Define: 
  1. Supervised learning 
     * Supervised learning is the machine learning task of inferring a function from labeled training data. The training data consist of a set of training examples. In supervised learning, each example is a pair consisting of an input object (typically a vector) and a desired output value.
  2. Features 
     * Attributes of the input data set
  3. Dependent Varaibles.
     * Its value is dependant on other variables y = f(x)
+ In the following figure, label features and independent variables:

![image](https://cloud.githubusercontent.com/assets/1433964/10419861/9b895770-7052-11e5-9fed-77c53a922a20.png)
<br>
     * outlook
     * temperature
     * humidity
     * windy
     * play

+ In a few lines, differentiate regression and classification.
  1. Regression
     * Output will be a possibe infinite numbers.  eg. predicting tomorrow's weather
  2. Classification
     * Output will be a discrete label. eg. predicting tomorrow's climate
+ What is risk exposure? Give a mathematical expression to calculate it.
  * ￼￼￼￼
+ Sort the steps taken in predicting delays, as proposed by Dr. Hoa:
  * Extract Features, and select the ones that contribute to risk of delay.
  * Characterize the issues that constitute delays.
  * Train classifiers. 
 <br>
  Answer
  * Characterize the issues that constitute delays.
  * Extract Features, and select the ones that contribute to risk of delay.
  * Train classifiers.
+ In the following figure label **A** and **B**:

![1](https://cloud.githubusercontent.com/assets/1433964/10259938/29db384a-693c-11e5-8163-69f25542da9a.png)

+ Define networked data
  * Data which has inter relationships. like social media, webpages 
+ Briefly describe task networks
  Task networks is a directed graph. V - tasks with (id,class and attributes) , E - link type and weights
+ Define: 
 1. Explicit relationship,
    * Explicitly mentioned in the task records. Typically determinf in which the tasks need to be performed. eg blockers
 2. Implicit relationship (give an example)
    * They need to be inferred from the other task's information. eg. tasks that share same resource(developer) , tasks that affect the same parts of the code.
 3. Resourse based relationship
    * this type of relationships exists between tasks that share the same (human) resource. two tasks are assigned to the same developer. 
 4. Attribute based relationship
    * tasks can be related if some of their attributes share the same values. tasks that affect the same part of the code. 
 5. Content based relationship.
    * tasks can be similar in terms of how they are conducted and/or what they affect


_________

<img align=right src="https://raw.githubusercontent.com/txt/mase/master/img/pd-icon.png">Copyright © 2015 [Tim Menzies](http://menzies.us).
This is free and unencumbered software released into the public domain.   
For more details, see the [license](https://github.com/txt/mase/blob/master/LICENSE.md).

