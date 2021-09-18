# RL_factor_search
Automated factor search algorithm

## Strategy tree
We model strategies with multiple factors as the tree below,
<br>
<img src='https://user-images.githubusercontent.com/73049948/133891607-0d94e23a-09c8-464f-bed3-ed5545adff4c.PNG' width=300>
<br>
<img src='https://user-images.githubusercontent.com/73049948/133891658-88fe670c-8e17-4e20-8776-4ac9a59eb0e6.PNG' width=500>
<br>
Also, Features such as netinc or gp are normalized with their marketcap. 
<br>
In order to maintain the robustness againt the outlier, we used only Rank function as an unnary.
<br>
Binaries used are +, -, X, and %. In the list notation, the above tree can be expressed as follows,


## Search Algorithm: Epsilon-greedy DQN
We use DQN to find the best tree. Network structure is currently on update.
<br>
1. State: List of binaries & features chosen so far.
2. Action: Next element: a single binary or feature.
3. Reward: If list becomes closed expression, reward = sharpe ratio. If list is not closed within the MAX_LEN, reward = -1. Else reward = 0.

## Current result
Reward plot
<br>
![reward](https://user-images.githubusercontent.com/73049948/133892479-4b49eb45-9bed-41db-b0c3-4c60d9c6dc14.png)
<br>
Some factors found so far.
<br>
<img src='https://user-images.githubusercontent.com/73049948/133892485-5308cac7-8024-4d74-8dae-bee665dc3147.PNG' width=500>
