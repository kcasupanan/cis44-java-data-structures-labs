public class Matrix {
    public static void main(String[] args) {
        Main m1 = new Main(3, 3);
        Main m2 = new Main(3, 3);

        m1.populateRandom();
        m2.populateRandom();

        System.out.println("Matrix 1:");
        System.out.println(m1);

        System.out.println("Matrix 2:");
        System.out.println(m2);

        try {
            Main sum = m1.add(m2);
            System.out.println("Sum of Matrix 1 and Matrix 2:");
            System.out.println(sum);
        } catch (IllegalArgumentException e) {
            System.out.println("Addition Error: " + e.getMessage());
        }
    }
}
  
