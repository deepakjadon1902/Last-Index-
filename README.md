import java.util.Scanner;
public class Main {
    public static int findLastIndex(int[] arr, int currentIndex, int M) {
        if (currentIndex < 0) {
            return -1;
        }
        if (arr[currentIndex] == M) {
            return currentIndex;
        }
        return findLastIndex(arr, currentIndex - 1, M);
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        int[] arr = new int[N];
        for (int i = 0; i < N; i++) {
            arr[i] = scanner.nextInt();
        }
        int M = scanner.nextInt();
        int result = findLastIndex(arr, N - 1, M);
        System.out.println(result);
    }
}

