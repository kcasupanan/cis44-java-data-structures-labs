public class Playlist_2 { 
public static void main(String[] args) {
    Playlist playlist = new Playlist();
    
    Song song1 = new Song("Third World", "BashfortheWorld");
    Song song2 = new Song("Viva La Vida", "Coldplay");
    Song song3 = new Song("Snooze", "SZA");

    // Create Song 1
    //Song song1 = new Song();
    //song1.title = "Third World";
    //song1.artist = "BashfortheWorld";

    // Create Song 2
    //Song song2 = new Song();
    //song2.title = "Viva La Vida";
    //song2.artist = "Coldplay";

    // Create Song 3
   //Song song3 = new Song();
    //song3.title = "Snooze";
    //song3.artist = "SZA";

    // Add songs to playlist
    playlist.addSong(song1);
    playlist.addSong(song2);
    playlist.addSong(song3);

    // Display playlist
    System.out.println("\n=== Display Playlist ===");
    playlist.displayPlaylist();

    // Play next song twice
    System.out.println("\n=== Play Next ===");
    playlist.playNext();
    playlist.playNext();

    // Remove a song
    System.out.println("\n=== Remove Song: Snooze ===");
    playlist.removeSong("Snooze");

    // Display updated playlist
    System.out.println("\n=== Updated Playlist ===");
    playlist.displayPlaylist();
}

    private static class song {

        private static void addSong(Song song1) {
            throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
        }

        public song() {
        }
    }
}
