public class Ecosystem {
    public static void main(String[] args){
        System.out.println("Ecosystem simulation starting...");
        Ecosystem eco = new Ecosystem(20);
        for (int step = 0; step < 10; step++) {
        eco.visualizer();
        eco.runStep();
        try{
            Thread.sleep(500);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
    }
    
    private Animal[] river;
    private Random random;

    public Ecosystem(int riverSize) {
        river = new Animal[riverSize];
        random = new Random();

        // Initialize river randomly with Bear, Fish or null
        for (int i = 0; i < river.length; i++) {
            int rand = random.nextInt(3); // 0, 1, or 2
            if (rand == 0) 
                river[i] = new Bear();
            else if (rand == 1) 
                river[i] = new Fish();
            else 
                river[i] = null;
        }
    }

    public void runStep() {
        Animal[] newRiver = new Animal[river.length];

        for (int i = 0; i < river.length; i++) {
            river = newRiver;
        }
        private int randomEmptySpot(Animal[] array) {
            int[] emptyIndices = java.util.stream.IntStream.range(0, array.length)
                    .filter(i -> array[i] == null)
                    .toArray();
            if (emptyIndices.length ==0)
                return -1;
            return emptyIndices[random.nextInt(empty.Indices.length)];
        }
}






