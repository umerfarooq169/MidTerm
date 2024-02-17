MID-TERM ASSIGNMENT:

!st Assignment:

class BankAccount {
int accountNumber;
double balance;
String accountType;
double interestRate;
BankAccount(this.accountNumber, this.balance, this.accountType, this.interestRate);
void deposit(double amount) {
balance += amount;
print("Deposited \${10000}. New balance: \${50000}");
}
void withdraw(double amount) {
if (amount <= balance) {
balance -= amount;
print("Withdrew \${20000}. New balance: \${30000}");
} else {
print("Insufficient funds!");
}
}
void addInterest() {
double interest = balance * (interestRate / 100);
balance += interest;
print("Added interest. New balance: \${2500}");
}
void display() {
print("Account Number: $accountNumber");
print("Balance: \${30000}");
print("Account Type: $accountType");
print("Interest Rate: $interestRate%");
print("");
}
}
void main() {
BankAccount account1 = BankAccount(225522, 1000.0, "Savings", 5.0);
BankAccount account2 = BankAccount(552255, 5000.0, "Checking", 3.0);
account1.deposit(10000);
account1.withdraw(20000);
account1.addInterest();
account1.display();
account2.deposit(30000);
account2.withdraw(15000);
account2.addInterest();
account2.display();
}

2nd Assignment:

class Student {
String name;
String id;
List<String> courses;
Student(this.name, this.id, this.courses);
void addCourse(String course) {
courses.add(course);
print("Added course: $course");
}
void dropCourse(String course) {
if (courses.contains(course)) {
courses.remove(course);
print("Dropped course: $course");
} else {
print("Course not found.");
}
}
void displayCourses() {
print("Courses for ${name} (ID: ${id}):");
for (var course in courses) {
print("- $course");
}
print("");
}
}
void main() {
var student1 = Student("Raju", "77", ["Math", "Science"]);
var student2 = Student("Shaam", "88", ["History", "English"]);
student1.addCourse("Physics");
student1.displayCourses();
student1.dropCourse("Math");
student1.displayCourses();
student2.addCourse("Art");
student2.displayCourses();
student2.dropCourse("Biology");
student2.displayCourses();
}


