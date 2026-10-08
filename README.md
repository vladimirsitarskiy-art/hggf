// Завдання 1 (Варіант 4): Прості арифметичні операції через switch-case
function calculate(num1, num2, operator) {
    let result;

    switch (operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 === 0) {
                return "Помилка: ділення на нуль заборонено!";
            }
            result = num1 / num2;
            break;
        default:
            return "Помилка: невідомий оператор!";
    }

    return `${num1} ${operator} ${num2} = ${result}`;
}

// Перевірка роботи
console.log(calculate(10, 5, '+')); // 10 + 5 = 15
console.log(calculate(20, 4, '/')); // 20 / 4 = 5
console.log(calculate(7, 3, '*'));  // 7 * 3 = 21
console.log(calculate(5, 0, '/'));  // Помилка: ділення на нуль заборонено!
