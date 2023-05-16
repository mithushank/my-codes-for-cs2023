#include <iostream>
#include <list>
using namespace std;

struct Node{
    int label;
    list<int> neighbours;
};

struct Graph{
    int n=9;
    Node* nodes = new Node[n];

    void intializenodes(){
        for(int i=1;i<n;i++){
            nodes[i].label = i;
        }
    }

    void addedge(int u, int v){
        nodes[u].neighbours.push_back(v);
        nodes[v].neighbours.push_back(u);
    }

    void print(){
        for(int i=0; i<n; i++){
            cout << "Node " << nodes[i].label << ": ";
            for(int neighbour : nodes[i].neighbours){
                cout << neighbour << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    Graph* g = new Graph;
    g->intializenodes();
    //add edges for the graphs here.
    g->addedge(1, 2);
    g->addedge(1, 3);
    g->addedge(1, 5);
    g->addedge(1, 4);
    g->addedge(2, 3);
    g->addedge(2, 6);
    g->addedge(4, 6);
    g->addedge(4, 7);
    g->addedge(4, 8);
    g->addedge(5, 6);
    g->addedge(5, 7);  
    g->addedge(5, 8);      
    //print the graph adjacency list
    g->print();

    delete g; // Free allocated memory
}
