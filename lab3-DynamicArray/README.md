public class Main {
    public static void main(String[] args) {
        DynamicArray<String> nflTeams =  new DynamicArray<>();
        
        nflTeams.add("Raiders");
        nflTeams.add("49ers");
        nflTeams.add("Chiefs");
        
        System.out.println("Total teams: " + nflTeams.size());
        
        System.out.println("Team at index 1: " + nflTeams.get(1));
        
        String removed = nflTeams.remove(2);
        System.out.println("Removed team: " + removed);
        
        System.out.println("Total teams after removal: " + nflTeams.size());
        
        System.out.println("Team still at index 0: " + nflTeams.get(0));
    }
}
