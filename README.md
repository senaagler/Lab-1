# Lab-1
Animals
package Lab_1;


abstract class Animal {
    String isim;
    int yas;

  
    public Animal(String isim, int yas) {
        this.isim = isim;
        this.yas = yas;
    }

    
    public void sesCikar() {
        System.out.println("Bu hayvan ses çıkarıyor!");
    }

   
    public void hareketEt() {
        System.out.println("Bu hayvan hareket ediyor!");
    }
}


class Cat extends Animal {

    
    public Cat(String isim, int yas) {
        super(isim, yas);
    }

    
    @Override
    public void sesCikar() {
        System.out.println("Miyav!");
    }

    
    public void oyuncakOyna() {
        System.out.println("Kedi oyuncakla oynuyor.");
    }
}


class Dog extends Animal {

   
    public Dog(String isim, int yas) {
        super(isim, yas);
    }

    
    @Override
    public void sesCikar() {
        System.out.println("Hav hav!");
    }

    
    public void topOyna() {
        System.out.println("Köpek top ile oynuyor.");
    }
}

class Bird extends Animal {

    
    public Bird(String isim, int yas) {
        super(isim, yas);
    }

    
    @Override
    public void sesCikar() {
        System.out.println("Cik cik!");
    }

    
    public void uc() {
        System.out.println("Kuş uçuyor.");
    }
}

public class lab7 {
    public static void main(String[] args) {
        Animal[] hayvanlar = {
            new Cat("Kedi", 2),
            new Dog("Köpek", 3),
            new Bird("Kuş", 1)
        };

        for (Animal hayvan : hayvanlar) {
            hayvan.sesCikar(); 
        }

        for (Animal hayvan : hayvanlar) {
            hayvan.hareketEt(); 
        }

        for (Animal hayvan : hayvanlar) {
            if (hayvan instanceof Cat) {
                ((Cat) hayvan).oyuncakOyna();
            } else if (hayvan instanceof Dog) {
                ((Dog) hayvan).topOyna();
            }
        }
    }
}
