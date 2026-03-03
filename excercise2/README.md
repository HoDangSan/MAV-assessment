# Project Name: Excercise 2
  Accordion & Tab Page by Vue 3

## 🚀 Main features
- Responsive interface.
- Integrated Tailwind CSS.

## 🛠️ Technology used
-  Vue 3 (typescript), Vite, SCSS, tailwind CSS.

## 📦 Installation instructions
- To run this project on your local machine, follow these steps:

1. Clone project:
- git clone https://github.com/HoDangSan/MAV-assessment.git

2. Setup Project
- cd excercise2
- npm install
 
3. Run Project
- npm run dev

## 🚀 Website
- https://mav-assessment-excercise2.vercel.app/

## 👀 Explain why the result of ('b' + 'a' + + 'a' + 'a').toLowerCase() is banana
- Start with 'b' + 'a'
    Concatenating two strings
    'b' + 'a' => 'ba'
- Next + 'a'
    The unary plus (+) operator tries to convert its operand into a number. And, 'a' is not a valid numeric string.
    so + 'a' becomes NaN (not a number)
    + 'a' => NaN
- Final, we have 'ba' + NaN + 'a' => 'baNaNa' => 'baNaNa'.toLowerCase() => 'banana'
