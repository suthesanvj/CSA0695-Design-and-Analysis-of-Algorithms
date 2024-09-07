#include <stdio.h>
#define INF 99999999

int n;
int dist[10][10];
int dp[1024][10];  // DP table
int visited_all;

int tsp(int mask, int pos) {
    if (mask == visited_all) {
        return dist[pos][0];
    }
    if (dp[mask][pos] != -1) {
        return dp[mask][pos];
    }
    
    int ans = INF;
    for (int city = 0; city < n; city++) {
        if ((mask & (1 << city)) == 0) {
            int newAns = dist[pos][city] + tsp(mask | (1 << city), city);
            ans = (ans < newAns) ? ans : newAns;
        }
    }
    return dp[mask][pos] = ans;
}

int main() {
    printf("Enter number of cities: ");
    scanf("%d", &n);
    
    printf("Enter the distance matrix:\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &dist[i][j]);
        }
    }

    visited_all = (1 << n) - 1;

    for (int i = 0; i < (1 << n); i++) {
        for (int j = 0; j < n; j++) {
            dp[i][j] = -1;
        }
    }

    printf("The minimum travelling cost is: %d\n", tsp(1, 0));

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153515](https://github.com/user-attachments/assets/6ca7e369-d1e6-45d4-94eb-8b6c36c75170)
