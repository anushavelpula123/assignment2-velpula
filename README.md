# assignment2-velpula
# Anusha Velpula

#### maryville

#### A&G this place has great variety and prices are decent.<br>It has lot of indian varieties.

**buttery popcorn**

**herseys syrup**

-----------------------------
# Airport Near Me Kansas City international Airport

Kansas City international Airport 1 international Square,kansas City,MO 64153

1. head soyth on N Frederick St toward W 1st St

2. Turn right onto W 1st St 50ft

3. Turn left onto S Munn Ave 450ft

4. Turn left onto s Hills Dr 1.5mi

5. Turn right onto US-71 BUS S/S Main St 0.5mi

6. Take the ramp to US-71 S 0.7mi

7. Take the i-29 S/US-71 S exit on the left toward US-59 S/Kansas City 0.4mi

8. Merge onto i-29 S/US-71 S 0.4mi

9. keep left at the fork to stay on i-29 S 31mi

10. keep right at the fork,follow signs for KCI Airport 0.3mi

11. Merge onto NW 120th St 1.5mi

12. Turn left onto E 9th St 
destination will be on the right.

### Some favourite dishes
* MEXICAN SALAD
* HOT DOGS
* REUBEN SANDWICH

Click [here](https://github.com/anushavelpula123/assignment2-velpula/blob/main/AboutMe.md) to go to AboutMe.md

-----------------------------------------------

# Sports

Below mentioned is a list of sports that I would recommend for anyone.

|  Name       |  Location   | Amount|
|-------------|-------------|-------|
|  Basketball | Recreation  |  $40  |
|  Volleyball | Recreation  |  $35  |
|  Soccer     | Recreation  |  $50  |
|  Tennis     | Recreation  |  $50  |

-------------------------------------------------

# Quotes

> There is nothing noble in being superior to your fellow man; true nobility is being superior to your former self - _ERNEST HEMINGWAY_

> If you’re always trying to be normal you will never know how amazing you can be - _MAYA ANGELOU_

--------------------------------------------------

# S Number - 3

> Given a connected and undirected graph, a spanning tree of that graph is a subgraph that is a tree and connects all the vertices together. A single graph can have many different spanning trees. A minimum spanning tree (MST) or minimum weight spanning tree for a weighted, connected, undirected graph is a spanning tree with a weight less than or equal to the weight of every other spanning tree. The weight of a spanning tree is the sum of weights given to each edge of the spanning tree. [Source-link](https://www.geeksforgeeks.org/kruskals-minimum-spanning-tree-algorithm-greedy-algo-2/)

```
struct Edge {
    int u, v, weight;
    bool operator<(Edge const& other) {
        return weight < other.weight;
    }
};

int n;
vector<Edge> edges;

int cost = 0;
vector<int> tree_id(n);
vector<Edge> result;
for (int i = 0; i < n; i++)
    tree_id[i] = i;

sort(edges.begin(), edges.end());

for (Edge e : edges) {
    if (tree_id[e.u] != tree_id[e.v]) {
        cost += e.weight;
        result.push_back(e);

        int old_id = tree_id[e.u], new_id = tree_id[e.v];
        for (int i = 0; i < n; i++) {
            if (tree_id[i] == old_id)
                tree_id[i] = new_id;
        }
    }
}
```
[Source-Code-Link](https://cp-algorithms.com/graph/mst_kruskal.html)
