50: Combination Sum II
solution:
class Solution {
    List<List<Integer>> ans;
    int candidates[];
    public List<List<Integer>> combinationSum2(int[] candidates, int target) {
      
        Arrays.sort(candidates);
        this.candidates=candidates;

        ans= new LinkedList();
        backtrack(0,target,new LinkedList<Integer>());
        return ans;

    }
    void backtrack(int start,int target, List<Integer> list)
    {

        if(target==0) {
            ans.add(new LinkedList(list));
        }
        if(target<0) return;
        for(int i=start;i<candidates.length;i++)
        {
            
            if(i>start && candidates[i]==candidates[i-1]) continue;

            list.add(candidates[i]);
            backtrack(i+1,target-candidates[i],list);
            list.remove(list.size()-1);
        }

    }
}