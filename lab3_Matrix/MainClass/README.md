import java.util.Random;

public class Main {
    private int[][] data;

    // Constructor: empty matrix
    public Main(int rows, int cols) {
        data = new int[rows][cols];
    }

    // Constructor: using pre-existing 2D array
    public Main(int[][] data) {
        this.data = data;
    }    
    
    public void populateRandom() {
        Random rand = new Random();
        for (int j = 0; j < data[i].length; j++) {
            data[i][j] = rand.nextInt(10) + 1;
        }
    }
}

public Main add(Main other) {
    if (this.data.length != other.data.length || this.data[0].length != other.data[0].length){
        throw new IllegalArgumentException("Matrix dimension must match for addition.");
    }
    
    int[][] result = new int [data.length][data[0].length];
    for (int i = 0; i < data.length; i++) {
        for (int j = 0; j < data[i].length; j++) {
            result[i][j] = this.data[i][j] + other.data[i][j];
        }
    }
    
    return new Main(result);
    
}

    // String representation of matrix
    @Override
    public String toString() {
        StringBuilder sb = new StringBuilder();
        for (int[] row : data) {
            for (int val : row) {
                sb.append(val).append("\t");
            }
            sb.append("\n");
        }
        return sb.toString();
    }
