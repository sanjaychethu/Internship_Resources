### **Question 2: Juice Machines**

Cars in Wonderland run on strawberry juice. Suppose there is a circle, and there are **m** juice machines on that circle. You are given an array of data in pairs:

1. The amount of juice that every juice machine has.
2. The distance from that juice machine to the next juice machine.

Your task is to find the **first point/station** from where a car will complete the circle, i.e., visit all the stations and return to the starting one (out of the given, point starts from 0).

The car will stop at each juice machine and has infinite capacity. It will keep going in the same direction until there is no juice left in the car or it reaches the starting point.

**Note**: Assume for 1 liter of juice, the car can go 1 unit of distance.

---

### **Input/Output Format**

- **Input**:  
  An array of pairs where each pair contains the amount of juice at a machine and the distance to the next machine.  
  Example:  
  ```
  4  
  5 7  
  7 6  
  8 4  
  5 4
  ```

- **Output**:  
  The index of the first starting point from which the car can complete the circle. If no such point exists, return -1.  
  Example:  
  ```
  1
  ```

---

### **Constraints**

- \(1 \leq N \leq 10^5\)  
- \(1 \leq \text{juice, distance} \leq 100\)

---

### **Example 1**

**Input**:  
```
4  
5 7  
7 6  
8 4  
5 4
```

**Output**:  
```
1
```

**Explanation**:  
Starting from the 1st point (7, 6), the car can complete the circle as the juice available at each point exceeds the distance to the next point.

---

### **Example 2**

**Input**:  
```
6  
2 3  
4 5  
6 7
```

**Output**:  
```
-1
```

**Explanation**:  
There is no point where one can start and complete a circle as the juice available would be insufficient to cover the distance between any two points.

---

### **Help Section**

- **Approach**:  
  1. Calculate the total juice and total distance. If total juice < total distance, return -1.  
  2. Simulate the journey starting from each point. If the juice becomes negative, reset the starting point.  
  3. Return the valid starting point or -1 if no such point exists.
