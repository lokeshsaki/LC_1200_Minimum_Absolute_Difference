class Solution {
    public List<List<Integer>> minimumAbsDifference(int[] arr) {
        List<List<Integer>> result = new ArrayList<>();
        // result.add(Arrays.asList())
        int n = arr.length;
        int min_Diff = Integer.MAX_VALUE;
        Arrays.sort(arr);
         for(int i = 0; i <= n-2 ; i++){
            int diff  = arr[i+1] - arr[i];
            if(diff < min_Diff){
              min_Diff = diff;
                result.clear();
                result.add(Arrays.asList(arr[i] , arr[i+1]));    
               }
                else if(diff == min_Diff){
            result.add(Arrays.asList(arr[i] , arr[i+1]));
            }
            }
            return result;
            }
            }
     
       
          
      
