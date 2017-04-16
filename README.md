## This is an illustration of Andrew Trask's Miniproject 4 - Understanding Inefficiencies in Neural Networks - https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101

Andrew brillantly explains in that Udacity Class around a Sentiment Analysis project, why ignoring input features that are equal to zero helps improve efficiencies when generating ouput layer.

As an explicit illustration, and out of a really simple example,
I have generated some time coding around this idea to help appreciate the gain.

input is a 1 x 10 array : [0,0,0,1,0,0,0,0,1,0]
weights is a 10 x 5 random array

output is the sum of the multiplication of input by weights
old_way : we sum the result of each single input by weights
new_way : we sum only the result of 1 feature value in input by weights

old_way and new_way gets same result in term of values.
BUT "new_way" is faster and more optimized since we reduce the number of needed operations.
That enables more and more appreciable reduction in time processing, as big as the input get dimensioned ( assuming we have a fair amount of zero value input features)

This code shows how faster "new_way" gets us ( for that dummy, but easy to understand, example )