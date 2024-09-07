#include <stdio.h>
#include <stdbool.h>

#define V 5

bool isSafe(int v, int graph[V][V], int path[], int pos) {
    if (graph[path[pos - 1]][v] == 0) return false;
    for (int i = 0; i < pos; i++) {
        if (path[i] == v) return false;
    }
    return true;
}

bool hamCycleUtil(int graph[V][V], int path[], int pos) {
    if (pos == V) {
        if (graph[path[pos - 1]][path[0]] == 1) return true;
        else return false;
    }

    for (int v = 1; v < V; v++) {
        if (isSafe(v, graph, path, pos)) {
            path[pos] = v;
            if (hamCycleUtil(graph, path, pos + 1) == true) return true;
            path[pos] = -1;
        }
    }
    return false;
}

bool hamCycle(int graph[V][V]) {
    int path[V];
    for (int i = 0; i < V; i++) path[i] = -1;

    path[0] = 0;
    if (hamCycleUtil(graph, path, 1) == false) {
        printf("Solution does not exist\n");
        return false;
    }

    printf("Hamiltonian Cycle: ");
    for (int i = 0; i < V; i++) printf("%d ", path[i]);
    printf("%d\n", path[0]);
    return true;
}

int main() {
    int graph[V][V] = {
        {0, 1, 0, 1, 0},
        {1, 0, 1, 1, 1},
        {0, 1, 0, 0, 1},
        {1, 1, 0, 0, 1},
        {0, 1, 1, 1, 0}
    };

    hamCycle(graph);
    
    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 154806](https://github.com/user-attachments/assets/3eaa9f38-780c-453d-8a0c-9ad0de535b77)