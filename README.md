# -Valid-Parentheses


public class aditya {
     static boolean   isValid(String s) {
        Stack<Character>st=new Stack();
            for(int i=0;i< s.lenght(); i++)
            {
                if(s.charAt(i)=='{'||s.charAt(i)=='['||s.charAt(i)=='(')
                {
                    st.push(s.charAt(i));
                }
                else if ( !st.empty() && ((s.charAt(i)==']' && st.peek()=='[')||
                       (s.charAt(i)=='}' && st.peek()=='{')||
                       (s.charAt(i)==')' && st.peek()=='(')))
                {
                    st.pop();
                }
                else
                {
                    st.push(s.charAt(i));
                }
                    
            }
        return st.empty()? true : false;
        
    }
    public static void main(String[] args)
    {
        String s="{[]})";
        boolean result= isValid(s);
        System.out.println(result);
    }
}
                                      
                                      
                                      
                                      
     ------------------------------------------------------------------------------------------
     ------------------------------------------------------------------------------------------
                                      
           Balanced Brackets
                                      
                                      
      public class aditya {
     static boolean   isValid(String s) {
        Stack<Character>st=new Stack();
            for(int i=0;i< s.lenght(); i++)
            {
                if(s.charAt(i)=='{'||s.charAt(i)=='['||s.charAt(i)=='(')
                {
                    st.push(s.charAt(i));
                }
                                      
                                      
                else{
                     if(stack.isEmpty())
                     {
                       return "no";
                       }
                         else{
                              char pop_val=stack.pop();
                              if (s.charAt(i)=='}' && pop_val != '{'){
                                      return "NO";}
                            else  if (s.charAt(i)==')' && pop_val != '('){
                                      return "NO";}
                            else  if (s.charAt(i)==']' && pop_val != '['){
                                      return "NO";}
                                      
                                      
                }
                     }
                           }
                                      
                     if(stack.isEmpty())
                      {
                        return "YES";
                       }
                       else
                        {
                        return "NO";
                         }
                                      
