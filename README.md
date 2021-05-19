# Artificial Intelligence Tic-Tac-Toe Game
In this game, we use the minimax algorithm to complement the game. We use the api to access game server and compete with other classmates. We shall be introducing a new function called Search(). This function evaluates all the available moves using minimax() and then returns the best move the maximizer can make. The pseudocode is as follows :
def search(board):
	best = Null
	for each move in board:
		if current move is better than best:
			best = current move 
	return best

To check whether or not the current move is better than the best move we take the help of minimax() function which will consider all the possible ways the game can go and returns the best value for that move, assuming the opponent also plays optimally 
The code for the maximizer and minimizer in the minimax() function is similar to search() , the only difference is, instead of returning a move, it will return a value. Here is the pseudocode :
function minimax(board, depth, isMaximizingPlayer):

    if current board state is a terminal state :
        return value of the board
    
    if isMaximizingPlayer :
        best = -INFINITY 
        for each move in board :
            value = minimax(board, depth+1, false)
            best = max( best, value) 
        return best
    else :
        best = +INFINITY 
        for each move in board :
            value = minimax(board, depth+1, true)
            best = min( best, value) 
        return best
![image](https://user-images.githubusercontent.com/60612585/118830832-d5e33b00-b8f1-11eb-8ecb-f4780814e6ca.png)

