# ossPractice

import java.util.*; // Scanner, StringTokeonizer, Arrays, Random 사용하려고 선언
import java.io.*; // Buffered, IOExeption, FileInputStream 사용하려고 선언

public class Main {
    public static void main(String[] args) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        StringTokenizer st = new StringTokenizer(br.readLine());

        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());
        int c = Integer.parseInt(br.readLine());

        if (b + c < 60) {
            b = b + c;
        }

        else {
            a += (b + c) / 60;
            b = (b + c) % 60;

            if (a >= 24) {
                a -= 24;
            }
        }

        System.out.println(a + " " + b);
    }
}
