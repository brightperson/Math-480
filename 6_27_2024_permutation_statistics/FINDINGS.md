# Summary of findings.

## Statistic 1
**Accuracy achieved:**
100%
**Description of model weights:**
The maps describe the likleyhood of any given number put in position $n$, with blue being less likley and red being more likley.
For example, if $n=5$,  Row 0 in the fives poition has a very dark blue box above 1 and 4 equally light light red boxes. This would be interpeted
as "the permutations that stat1 labels 0 are extremly unlikley to have a 1 in the fives position and have equal distribution for all other numbers"
For these weights, It seems to have a general pattern of a strong weight (blue for row 0 and red for row 1) in the first entry of the last bar for both, with the 
rest of the wheits seeming to revolve around the distribution(all other bars have a small weight in each first entry, rest of entries in last bar are slightly the opposite color).
**How to compute statistic:**
If there is a 1 in the last posiition of the permuation, label 1. Otherwise, label 0.

## Statistic 2
**Accuracy achieved:**
100%
**Description of model weights:**
For row 1, Any difference in model weights is focused on the last two entries, with the second-to-last showing a great bias towards
the upper half of avialible letters (for example, if n=6 it's more likley to choose 4,5,6) and the last showing a great bias towards the lower half (1,2,3 in the n=6 case). Row 0 seems to be the exact inverse.
**How to compute statistic:**
If the last two entries of the permutation are in decending order, its value is 1. Otherwise, its value is 0

## Statistic 3
**Accuracy achieved:**
Test accuracy = 95.83333333333333%
Training acuraccy = 99.47916666666667%
**Description of model weights:**
The model has 2 main trasformations, with one going from 2 to 6 and the other going from 6 to 36. From there, though, there aren't any discernable patterns visible within the heatmap, even though whatever method the model came up with is reativley accurate.
**How to compute statistic:**
Findings not signifiagant enough for a definitive answer
## Statistic 4
**Accuracy achieved:**
100.0%
**Description of model weights:**
In row 1, each connection between a number and itself is labeled extremely unlikely (with the inverse being implied for row 0). 
**How to compute statistic:**
If there is at least 1 entry that the given permuation shares in the same position with (1,2,3,4,5), label that permuation 0. Label as 1 otherwise.
## Statistic 5
**Accuracy achieved:** 
Got a divide by zero error on the accuracy for test
training: 45.833333333333336
**Description of model weights:**
As a whole, the weights are pretty impossible to describe, but the first and last rows seem to indicate that the values of 0 and 10 map onto combianations of (12345) and (54321) respecitively, as the heatmap shows a strong preference for those entries in that order. Otherwise, there seems to be no general pattern.
**How to compute statistic:**
Complete guess, but maybe the amount of times you need to swap two numbers from (12345) in order to get a given combination
## Statistic 6
**Accuracy achieved:**
Test accuracy = 31.944444444444443
Training accuracy = 55.38194444444444%
**Description of model weights:**
Hard to gauge as the acuraccy is quite low, and there didn't seem any way to get it signifigantly higher. No real evidence of any patterns
**How to compute statistic:**
Not  discernibe with such limited information
## Statistic 7
**Accuracy achieved:**
53.125%
**Description of model weights:**
First and last last rows indicate that (12345) and (54321) have values 0 and n-1, but all values in between have no discernible pattern
**How to compute statistic:**
Set (12345) to 0 and (54321) to n-1. Beyond that, impossible to tell.
## Statistic 8
**Accuracy achieved:**
test accuracy = 73.61111111111111%
training accuracy = 80.03472222222223%
**Description of model weights:**
General bias of earlier values in index 6 such as 1,2,3 and later values such as 5,6 in index 1, but overall no discerable pattern
**How to compute statistic:**
impossible to discern with current rates of accuracy.
## Statistic 9
**Accuracy achieved:**
test accuracy = 80.55555555555556%
training accuracy =  83.50694444444444%
**Description of model weights:**
Seems to be a general "rule of threes" going from right to left. Index 6 has a greater liklihood for (4,5,6), index 5 has a greater liklihood for (3,4,5), and so on. However, I'm not able to think of a rule for this that would also adhere to all of the resirictions of what's acually in permutations6.csv
**How to compute statistic:**
impossible to discern with current rates of accuracy.