        # TransferListTo-.txt


        import java.io.FileWriter;
        import java.io.IOException;
        import java.util.LinkedHashMap;

        public class TransferListTotxt {

        public static void main(String[] args) throws IOException {
        LinkedHashMap<Integer, Student> iSLHM = new LinkedHashMap<>(6, 0.75f, true);

        Student student1 = new Student("Nikita", "Sidjey", 3);
        Student student2 = new Student("Mike", "Mayer", 2);
        Student student3 = new Student("Jack", "Impover", 1);
        Student student4 = new Student("Angelina", "Jolie", 1);
        Student student5 = new Student("Oliver", "Constant", 2);
        Student student6 = new Student("Thomas", "Shelby", 3);

        iSLHM.put(01010, student1);
        iSLHM.put(02020, student2);
        iSLHM.put(03030, student3);
        iSLHM.put(04040, student4);
        iSLHM.put(05050, student5);
        iSLHM.put(06060, student6);

        String transfer = iSLHM.toString();

        FileWriter writer = null;

        try {
            writer = new FileWriter("TransferListTo.txt");
            for (int i = 0; i < transfer.length(); i++) {
                writer.write(transfer.charAt(i));
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            writer.close();
          }

        }

    }


    class Student {
    String name, surname;
    int course;

    public Student(String name, String surname, int course) {
        this.name = name;
        this.surname = surname;
        this.course = course;
    }

    @Override
    public String toString() {
        return "Student: " + "name='" + name + '\'' + ", surname='" + surname + '\'' + ", course=" + course + ';' + "\n";
        }
    }
