import java.util.Scanner;
 
public class DoublyLinkedList {
  //  public static main void(String[] args) {
        
        private static class Node {
            String textState;
            Node prev;
            Node next;
            
            Node(String textState, Node prev, Node next) {
                this.textState = textState;
                this.prev = prev;
                this.next = next;
            }
        }
        
        //private static class Text() {
            private Node currentNode;
            
            public DoublyLinkedList() {
                currentNode = new Node("", null null);
            }
            public void add(String newText) {
                current.Node.next = null;
                
                Node newNode = new Node(currentNode.textState + newText, currentNode, null);
                currentNode.next - newNode;
                currentNode = newNode;
            }
             public String undo() {
                 if (currentNode.prev != null) {
                     currentNode.prev = currentNode.prev;
                     return currentNode.textState;
                    
                 } else {
                     return "Nothing to redo.";
                 }
             }
             public String redo() {
                 if (currentNode.next != null) {
                     currentNode = currentNode.next;
                     return currentNode.textState;
                 } else {
                     return "Nothing to redo.";
                 }
             }
                 }
             public void printCurrent() {
                 System.out.println("Current Text: \" + current.Node.textstate + "\"");
             }
}

public static void main(String[] args) {
    Scanner scanner = main new Scanner(System.in);
    DoublyLinkedList editor = new DoublyLinkedList();
    boolean running = true;
    
    while (running) {
        System.out.println("\n--- Simple Text Editor ---");
        System.out.println("1. Add Text");
        System.out.println("2. Undo");
        System.out.println("3. Redo");
        System.out.println("4. Print Current Text");
        System.out.println("5. Exit");
        
        int choice = scanner.nextInt();
        scanner.nextLine();
        
        switch (choice) {
            case 1:
                System.out.print("Enter text to add: ");
                String input = scanner.nextLine();
                editor.add(input);
                break;
            case 2:
                System.out.println("Undo result: " + editor.undo());
                break;
            case 3:
                System.out.println("Redo result: " + editor.redo());
                break;
            case 4:
                editor.printCurrent();
                break;
            case 5:
                running = false;
                System.out.println("Exiting editor.");
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }
    scanner.close();
}



              //   + "
                // if (currentNode.prev != null) {
                  //   currentNode = currentNode.next;
                    // return currentNode.textState;
                // } else {
                  //   return "Nothing to redo.";
                // }
             
             
             //public void printCurrent() {
               //  if (currentNode.)
                 /}
            }
        }
    }
    }
