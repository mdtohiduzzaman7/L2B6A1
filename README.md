1.   What are some differences between interfaces and types in TypeScript?

  Interface: সাধারণত অবজেক্টের কাঠামো নির্ধারণের জন্য ব্যবহৃত হয়।

  Example:
  interface Person {
    name: string;
    age: number;
  }

Type alias: এটি যে কোনো ধরনের টাইপকে একটি নাম দিতে পারে। যেমন primitive type, union type, tuple ইত্যাদি।
Example:

type ID = string | number;
type Point = { x: number; y: number };


3.  Explain the difference between any, unknown, and never types in TypeScript?

---> any

any টাইপ দিয়ে TypeScript-কে বলা হয় যে এই ভ্যারিয়েবলের কোনো টাইপ চেক করার দরকার নেই।

let data: any;
data = 10;
data = "Hello";
data = true;

---> unknown

unknown ভ্যারিয়েবলে যেকোনো টাইপের মান রাখা যায়, কিন্তু directly অপারেশন করা যাবে না।

let value: unknown;
value = 10;
value = "Hello";

if (typeof value === "string") {
    console.log(value.toUpperCase());
}

console.log(value.toUpperCase()); 

---> never

never টাইপ বোঝায় এই ভ্যারিয়েবল কখনো কোনো ভ্যালু নেবে না।

function error(message: string): never {
    throw new Error(message);
}

function infiniteLoop(): never {
    while(true) {}
}
