import java.util.ArrayList;

public class Playlist {
    private ArrayList<Song> songs;
    private int currentIndex;

    public Playlist() {
        songs = new ArrayList<>();
        currentIndex = 0;
    }

    public void addSong(Song song) {
        songs.add(song);
    }

    public void displayPlaylist() {
        for (Song song : songs) {
            System.out.println(song.getTitle() + " by " + song.getArtist());
        }
    }

    public void playNext() {
        if (currentIndex < songs.size()) {
            Song next = songs.get(currentIndex);
            System.out.println("Now playing: " + next.getTitle() + " by " + next.getArtist());
            currentIndex++;
        } else {
            System.out.println("End of playlist.");
        }
    }

    public void removeSong(String title) {
        songs.removeIf(song -> song.getTitle().equalsIgnoreCase(title));
    }
}
