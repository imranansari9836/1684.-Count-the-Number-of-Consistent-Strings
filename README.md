class Solution {
    public int countConsistentStrings(String allowed, String[] words) {
        HashSet<Character> set=new HashSet<>();
        for(char ch:allowed.toCharArray())
        {
            set.add(ch);//ab
        }
        int count=0;
        for(String w:words)
        {
            boolean match=true;
           for(char ch:w.toCharArray())
           {
               if(!set.contains(ch))
               {
                   match=false;
                   break;
               }
           }
           if(match)
           {
               count++;
           } 
        }
        return count;
    }
}
