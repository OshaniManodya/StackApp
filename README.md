public class StackApp {

    
     
    public static void main(String[] args) {
        BoundedArrayStack theStack = new BoundedArrayStack(5);//create a stack with max size
        //push operation
        for(int i=1;i<=6;i++)
        {
            if(!theStack.isFull()){//insert items
            theStack.push(i*10);
        }
        else{
            System.out.print("Cannot push.Stack is full");
        }
      }
        theStack.print();
    
        //peek the top element
        if(!theStack.isEmpty())
        {
            System.out.print("Top element is: " + theStack.peek());
        }
        else{
            System.out.print("stack is empty, nothing to peek");
        }
        
        //pop operation
        if(!theStack.isEmpty()){
            while(!theStack.isEmpty()){
                //until the stack is empty, delete items from stack
                int val=theStack.pop();
                System.out.print(val);
                System.out.print("  ");
            }
        }
        else{
            System.out.print("Cannot pop ,stack is empty");   
        }
            
    }
    

}
