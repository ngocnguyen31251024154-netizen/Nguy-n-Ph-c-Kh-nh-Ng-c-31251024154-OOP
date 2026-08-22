using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace 31251024154
{
    using System;

    public class Student
    {
        private string name;
        private double score;
        private static int totalStudents = 0;

        public Student(string name, double score)
        {
            this.name = name;
            this.score = score;
            totalStudents++;
        }

        // TODO: write instance methods here
        public string GetName()
        {
            return name;
        }

        public double GetScore()
        {
            return score;
        }

        public bool IsPassed()
        {
            return score >= 5.0;
        }

        public string GetClassification()
        {
            if (score >= 8.0) return "Excellent";
            if (score >= 6.5) return "Good";
            if (score >= 5.0) return "Average";
            return "Weak";
        }

        // TODO: write static methods here
        public static int GetTotalStudents()
        {
            return totalStudents;
        }

        public static Student FindTopStudent(Student[] students)
        {
            Student top = students[0];
            for (int i = 1; i < students.Length; i++)
            {
                if (students[i].GetScore() > top.GetScore())
                {
                    top = students[i];
                }
            }
            return top;
        }

        public static double CalculateAverageScore(Student[] students)
        {
            double sum = 0;
            foreach (Student s in students)
            {
                sum += s.GetScore();
            }
            return sum / students.Length;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // TODO: create array of Student objects
            Student[] students = new Student[]
            {
            new Student("An", 8.5),
            new Student("Binh", 6.0),
            new Student("Chi", 4.5),
            new Student("Dung", 7.0),
            new Student("Em", 9.2)
            };

            // TODO: call static and instance methods as required
            Console.WriteLine("Total students: " + Student.GetTotalStudents());

            Console.WriteLine("\n-- Student list --");
            foreach (Student s in students)
            {
                string status = s.IsPassed() ? "Passed" : "Failed";
                Console.WriteLine($"{s.GetName()} - Score: {s.GetScore()} - {s.GetClassification()} - {status}");
            }

            Student top = Student.FindTopStudent(students);
            Console.WriteLine($"\nTop student: {top.GetName()} with score {top.GetScore()}");

            double avg = Student.CalculateAverageScore(students);
            Console.WriteLine($"Class average score: {avg:F2}");
        }
    }


}
