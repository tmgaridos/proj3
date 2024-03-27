namespace topic_3_programming_csharp
{
    internal class Program
    {
        static void Main(string[] args)
        {
            var random = new Random();

            int totalQuestions = random.Next(5, 16);
            int correctAnswers = 0;
            int questionCount = 0;

            Console.WriteLine($"Total number of questions: {totalQuestions}");
            for (int i = 0; i < totalQuestions; i++)
            {
                int firstOperand = random.Next(1, 15);
                int secondOperand = random.Next(1, 10);
                string[] operators = ["+", "-", "/", "*"];
                int oper = random.Next(0, operators.Length);
                int correctAnswer = 0;

                Console.WriteLine($"Question {i + 1}: What is {firstOperand} {operators[oper]} {secondOperand}");
                Console.WriteLine("Your answer: ");
                string? answer = Console.ReadLine();
                int actualAnswer = 0;

                switch (operators[oper])
                {
                    case "+":
                        correctAnswer = firstOperand + secondOperand;
                        break;
                    case "-":
                        correctAnswer = firstOperand - secondOperand;
                        break;
                    case "/":
                        correctAnswer = firstOperand / secondOperand;
                        break;
                    case "*":
                        correctAnswer = firstOperand * secondOperand;
                        break;
                }

                bool validNumber = int.TryParse(answer, out actualAnswer);

                if (validNumber == false)
                {
                    Console.WriteLine("Please enter a valid number."); 
                    break;
                }

                if (correctAnswer == actualAnswer)
                {
                    correctAnswers++;
                    Console.WriteLine("Correct!\n");
                }
                else
                {
                    Console.WriteLine($"\nIncorrect! The correct answer is {correctAnswer}.");
                }

                questionCount++;
            }

            decimal totalPercentage = (decimal) correctAnswers / (decimal) questionCount;

            Console.WriteLine("Results:");
            Console.WriteLine($"Total correct answers: {correctAnswers}");
            Console.WriteLine($"Percentage of correct answers: {totalPercentage:P2}%");
        }
    }
}
