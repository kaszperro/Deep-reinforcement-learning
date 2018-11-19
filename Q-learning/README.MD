Q-Learning is sort of dynamic programming, 
It creates an array, which maps states to rewards of taking actions, ex:
for this state (ex. position(1,2)) if you go left, you will receive 4 points, if you go right you will receive -3 points.

Update rule: 
qtable[state, action] = qtable[state, action] + learning_rate * (reward + gamma * np.max(qtable[new_state, :]) - qtable[state, action])
