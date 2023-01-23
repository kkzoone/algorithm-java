```java
import java.util.*;
class Solution {
    public int[] solution(int[] array, int[][] commands) {
        List<Integer> list = new ArrayList<>();
        int [] answer = new int[commands.length];
        
        for(int i=0; i< commands.length; i++){
            int start = commands[i][0]; 
            int end = commands[i][1]; 
            int k = commands[i][2]; 

            for(int j=start; j<=end; j++){
                list.add(array[j-1]);
            }
            Collections.sort(list);
            answer[i] = list.get(k-1);
            list.clear();
        }
        return answer;
    }
}
```
