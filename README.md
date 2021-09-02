# assignment2-Kondru
# Jitendra Kondru
#### Bora Bora

Best **Romantic Destination Island** and very **Beautiful Beaches** where we can find some peace. The Place is lot of fun and have various adventure activities like jetski, paddleboard, outrigger canoes, sail boats, catamarans, or glass submarine.

***
# Directions From Maryville to Worlds of Fun
1. Maryville
2. Head west on E 1st toward N Main St.
3. Turn left ont US-71 Bus S/S Main St.
    1. Continue to follow US -71 Bus
    2. Pass by Pizza Hut(on the right in 0.5mi)
4. Take the ramp to US -71 S
    1. use the left lane to take the i-29 exit
    2. Merge with i-29
    3. keep right at the Y junction to continue on i-435 E
    4. Take exit 54 for 48st toward Parvin rd.
5. Continue straight onto N Randolph Rd
    1. Sharp left onto Worlds of fun Ave
    2. Turn right
    3. Slight right
    4. Turn left
    5. Turn right
    6. Turn right 
6. Destination to Worlds of Fun Reached.
* Swimsuit
* BackPack
    * Towel
    * Sunscreen
    * Empty water bottle
* stroller or wagon if you have older kids
* flip flops for water park
* Definitely Some Active Friends

**[Go to AboutMe File](AboutMe.md)**


-----

# TABLES

This Table Data is related to Famous Indian spicy Dishes available in India.

| Food/Drink  |     Location      |  Amount |
|----------|:-------------:|------:|
| Chicken DumBiryani |  Hyderabad,India | $4 |
| Gongura Mutton |    Guntur,India   |   $5 |
| Chicken Mandi | Vijayawada,India |    $12 |
| Bongulo Chicken| Araku,India | $3|

-------

# Pithy Quotes

> Never hate your enemies. It affects your judgment - *Maria Puzo*

> You only live once, but if you do it right, once is enough — *Mae West*

------

# Code Fencing

> A bipartite graph is possible if the graph coloring is possible using two colors such that vertices in a set are colored with the same color. Note that it is possible to color a cycle graph with even cycle using two colors.Refer this site for more info <https://www.geeksforgeeks.org/bipartite-graph/>

```
{
int n;
vector<vector<int>> adj;

vector<int> side(n, -1);
bool is_bipartite = true;
queue<int> q;
for (int st = 0; st < n; ++st) {
    if (side[st] == -1) {
        q.push(st);
        side[st] = 0;
        while (!q.empty()) {
            int v = q.front();
            q.pop();
            for (int u : adj[v]) {
                if (side[u] == -1) {
                    side[u] = side[v] ^ 1;
                    q.push(u);
                } else {
                    is_bipartite &= side[u] != side[v];
                }
            }
        }
    }
}

cout << (is_bipartite ? "YES" : "NO") << endl;
}
```
Code Source <https://cp-algorithms.com/graph/bipartite-check.html>