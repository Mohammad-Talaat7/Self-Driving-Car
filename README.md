# Self-Driving-Car

This project utilizes a simple Artificial Neural Network (ANN) to operate.

The essence of an Artificial Neural Network revolves around predicting the values of all feasible actions in the current state, comparing them to previously acquired Q-values. This comparison is achieved through a designated loss function, expressed by the mathematical equation:

```math
𝐿 = \sum(𝑄𝑡𝑎𝑟𝑔𝑒𝑡 - 𝑄)^2
```

Once we have obtained the Q-values, we embark on the pivotal task of selecting an action, employing various action selection policies:

€ - Greedy:
In this policy, the model astutely favors the action with the highest Q-value, factoring in the parameter €. For instance, setting € to 0.1 signifies that the model will opt for the best action 90% of the time, while allocating 10% to explore and embrace the element of randomness.

€ - Soft (1 - €):
This policy takes the opposite stance, favoring the action with the highest Q-value relative to (1 - €). A € value of 0.1 indicates that a mere 10% of the time will the model adhere to the optimal action, leaving 90% for uninhibited exploration and unpredictability.

Softmax:
Distinguished from € - Greedy and € - Soft, the softmax function delicately transforms all outputs into a range between 0 and 1, subsequently scaled up by a factor of 100. This remarkable transformation endows the Q-values with probabilities, dictating the likelihood with which the model selects actions.

The essence shared by these action selection policies lies in striking a delicate balance between exploration and exploitation. A judicious blend of the two is crucial, as incessant exploration may yield inferior rewards, while unwavering exploitation risks hindering the model's capacity to learn and restrains it to random behavior.


In our Model we use softmax function to select action and Kivy to Create our Environment
