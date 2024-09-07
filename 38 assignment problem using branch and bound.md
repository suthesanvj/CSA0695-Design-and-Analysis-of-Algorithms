#include <stdio.h>
#include <limits.h>

#define N 4

int costMatrix[N][N] = {
    {9, 2, 7, 8},
    {6, 4, 3, 7},
    {5, 8, 1, 8},
    {7, 6, 9, 4}
};

int assignmentCost(int mask, int person, int dp[]) {
    if (person >= N) return 0;
    if (dp[mask] != -1) return dp[mask];

    int minCost = INT_MAX;
    for (int i = 0; i < N; i++) {
        if (!(mask & (1 << i))) {
            minCost = (minCost < (costMatrix[person][i] + assignmentCost(mask | (1 << i), person + 1, dp))) ? minCost : (costMatrix[person][i] + assignmentCost(mask | (1 << i), person + 1, dp));
        }
    }
    return dp[mask] = minCost;
}

int main() {
    int dp[1 << N];
    for (int i = 0; i < (1 << N); i++) dp[i] = -1;
    
    printf("Minimum assignment cost: %d\n", assignmentCost(0, 0, dp));
    
    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;![Screenshot 2024-09-07 154723](https://github.com/user-attachments/assets/a0c94fa7-192c-44c0-927a-6bdd5bc3d4fa)

}
![Screenshot 2024-09-07 154723](https://github.com/user-attachments/assets/bf23baae-32c7-4305-89a5-3caf28b8afb5)
