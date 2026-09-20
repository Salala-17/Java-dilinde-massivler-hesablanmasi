import java.util.Arrays;

public class MassivHesablanmasi {
    public static void main(String[] args) {
        // Hesablanacaq massiv
        int[] ededler = {12, 45, 67, 8, 23, 89, 34, 2};

        // Massivin elementləri
        System.out.println("Massiv: " + Arrays.toString(ededler));

        // Dəyişənlərin ilkin təyini
        int cem = 0;
        int max = ededler[0];
        int min = ededler[0];

        // Massiv üzərində dövr (for-each)
        for (int eded : ededler) {
            // Cəmin hesablanması
            cem += eded;

            // Maksimumun tapılması
            if (eded > max) {
                max = eded;
            }

            // Minimumun tapılması
            if (eded < min) {
                min = eded;
            }
        }

        // Ədədi ortanın hesablanması (kəsr hissəni itirməmək üçün double tipinə çevrilir)
        double edediOrta = (double) cem / ededler.length;

        // Nəticələrin çap edilməsi
        System.out.println("--------------------------------");
        System.out.println("Elementlərin cəmi: " + cem);
        System.out.println("Ədədi orta: " + edediOrta);
        System.out.println("Ən böyük element (Max): " + max);
        System.out.println("Ən kiçik element (Min): " + min);
    }
}
