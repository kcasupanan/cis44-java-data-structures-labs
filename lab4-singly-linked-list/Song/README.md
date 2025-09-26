public class Song {
    private String title;
    private String artist;
    // Constructor and getters...

    //Song(String third_World, String bashfortheWorld) {
        //throw new UnsupportedOperationException("Not supported yet.");
        // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    

    //void displayPlaylist() {
        //throw new UnsupportedOperationException("Not supported yet."); 
// Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody

    Song(String third_World, String bashfortheWorld) {
      //  throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    }

    public String getTitle() {
        //throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
        return null;
        //throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    }

    public String getArtist() {
        //throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    }
 

    

//public class Song {
    private static class Node {
        Song song;
        Node next;
        
        public Node(Song song) {
            this.song = song;
            this.next = null;
        }
    }
        // Node constructor...

    private Node head;
    private Node tail;
    private Node currentNode;
    private int size;

    public Song() {
        this.head = null;
        this.tail = null;
        this.currentNode = null;
        this.size = 0;
    }

    public void addSong(Song song) {
        Node newNode = new Node(song);
        if (head == null) {
            head = newNode;
            tail = newNode;
        } else {
            tail.next = newNode;
            tail = newNode;   
        }
        size++;
    }
        // Your implementation here...
    

    public void removeSong(String title) {
        Node prev = null;
        Node current = head;
        
        while (current != null) {
            if (current.song.title.equalsIgnoreCase(title)) {
                if (prev == null) {
                    head = current.next;
                }
                if (current == tail) {
                    tail = prev;
                }
                
                size--;
                System.out.println("Removed song: " + title);
                return;
            }
            prev = current; 
            current = current.next;
        }
        
        System.out.println("Removed song: " + title);
    }

// Handle two cases: removing the head and removing from elsewhere.
        // Don't forget to update the tail if the last song is removed.
 
    public void playNext() {
        if (currentNode == null) {
            currentNode = head;
        } else {
            currentNode = currentNode.next;
        }
        if (currentNode == null) {
            currentNode = head;
        }
        if (currentNode != null) {
            System.out.println("Now Playing: " + currentNode.song.title + " by " + currentNode.song.artist);
        } else {
            System.out.println("No songs in playlist.");
        }
    }
        // If currentNode is null, start from the head.
        // Otherwise, advance to the next node.
        // If you reach the end, loop back to the head.
    public void displaySong() {
        Node temp = head;
        System.out.println("Playlist:");
        while (temp != null) {
            System.out.println("- " + temp.song.title + " by " + temp.song.artist);
            temp = temp.next;
        }
    }
}
        // Traverse from the head and print each song.

      
