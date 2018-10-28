# praktika6ikbo16-17
# Терентьев Павел Вадимович

<pre>
import java.util.Random;

public class Main {
    public static void selectionSort(Student[] arr){
        for (int i = 0; i < arr.length; i++) {
            int min = arr[i].getId();
            int min_i = i;
            for (int j = i+1; j < arr.length; j++) {
                if (arr[j].getId() < min) {
                    min = arr[j].getId();
                    min_i = j;
                }
            }
            if (i != min_i) {
                Student tmp = arr[i];
                arr[i] = arr[min_i];
                arr[min_i] = tmp;
            }
        }
    }

    public static void main(String[] args)
    {
        Student[] st = new Student[10];
        Random random = new Random();
        int id = 0;
        for (int i = 0; i < st.length ; i++)
        {
            st[i] = new Student(random.nextInt(1000));
        }
        selectionSort(st);
        for (int i = 0; i < st.length ; i++)
        {
            System.out.println(st[i].toString());
        }
    }
}


// Student.java
public class Student {
    public int id;
    public String name;

    public Student()
    {
        id = 0;
    }

    public Student(int id)
    {
        this.id = id;
        this.name = "Вася";
    }

    public int getId() {

        return id;
    }

    public void setId(int id) {

        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    @Override
    public String toString()
    {
        return "Студент: " + getId() + ", имя: " + getName();
    }
}

// Студент: 7, имя: Вася
// Студент: 234, имя: Вася
// Студент: 291, имя: Вася
// Студент: 322, имя: Вася
// Студент: 493, имя: Вася
// Студент: 600, имя: Вася
// Студент: 864, имя: Вася
// Студент: 925, имя: Вася
// Студент: 930, имя: Вася
// Студент: 967, имя: Вася
</pre>
