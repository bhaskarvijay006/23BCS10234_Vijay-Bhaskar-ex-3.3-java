# 23BCS10234_Vijay-Bhaskar-ex-3.3-java


// Base class
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  getDetails() {
    return `${this.name}, Age: ${this.age}`;
  }
}

// Student subclass
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this.grade = grade;
  }

  getDetails() {
    return `${super.getDetails()}, Grade: ${this.grade}`;
  }
}

// Teacher subclass
class Teacher extends Person {
  constructor(name, age, subject) {
    super(name, age);
    this.subject = subject;
  }

  getDetails() {
    return `${super.getDetails()}, Subject: ${this.subject}`;
  }
}

// Example usage
const s = new Student("Aanya", 17, "12th");
const t = new Teacher("Mr. Rao", 42, "Mathematics");

console.log(s.getDetails()); // Aanya, Age: 17, Grade: 12th
console.log(t.getDetails()); // Mr. Rao, Age: 42, Subject: Mathematics
