// DynamicArray.java
public class DynamicArray<T> {
    private T[] data;
    int size;
    private static final int INITIAL_CAPACITY = 10;

    @SuppressWarnings("unchecked")
    public DynamicArray() {
        data = (T[]) new Object[INITIAL_CAPACITY];
        size = 0;
    }

    public void add(T element) {
        if (size == data.length) {
            resize();
        }
        data[size] = element;
        size++;
    }

    public T get(int index) {
        if (index < 0 || index >= size) {
            throw new IndexOutOfBoundsException("Index out of bounds.");
        }
        return data[index];
    }

    public T remove(int index) {
        if (index < 0 || index >= size) {
            throw new IndexOutOfBoundsException("Index out of bounds.");
        }

        T removed = data[index];

        // Shift elements to the left
        for (int i = index; i < size - 1; i++) {
            data[i] = data[i + 1];
        }

        data[size - 1 ] = null;
        size--;
        return removed;
    }

    public int size() {
        return size;
    }

    @SuppressWarnings("unchecked")
    private void resize() {
        T[] newData = (T[]) new Object[data.length *2];
        for (int i = 0; i < data.length; i++) {
            newData[i] = data [i];
        }
        data = newData;
    }

    String size(int i) {
        throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    }
}
