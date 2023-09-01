Car Operations
This code performs various operations on an array of cars.

Task 1
Create a new array of objects based on the old array, with only the "brand" and "isDiesel" properties.


Copied! ✅
📝 Copy Code
➕ Insert Code
const newCars = cars.map((car) => {
  return { brand: car.brand, isDiesel: car.isDiesel }
});

console.log(newCars);
Task 2
Create a new array that includes only the cars with a diesel engine.


Copied! ✅
📝 Copy Code
➕ Insert Code
const dieselCars = cars.filter((car) => car.isDiesel);
console.log(dieselCars);
Task 3
Create a new array that includes only the cars without a diesel engine.


Copied! ✅
📝 Copy Code
➕ Insert Code
const nonDieselCars = cars.filter((car) => !car.isDiesel);
console.log(nonDieselCars);
Task 4
Calculate the total price of all non-diesel cars.


Copied! ✅
📝 Copy Code
➕ Insert Code
const sum = cars
  .filter((car) => !car.isDiesel)
  .map((car) => car.price)
  .reduce((acc, price) => acc + price, 0);
console.log(sum);
Task 5
Increase the price of all cars in the array by 20%.


Copied! ✅
📝 Copy Code
➕ Insert Code
cars.forEach((car) => car.price *= 1.2);
console.log(cars);
Task 6
Create a new array where all diesel cars are replaced with a new car object.


Copied! ✅
📝 Copy Code
➕ Insert Code
const cars2 = cars.map((car) => {
  if (car.isDiesel) {
    return { brand: "Tesla", price: 25000, isDiesel: false };
  }
  return car;
});

console.log(cars2);
Alternatively:


Copied! ✅
📝 Copy Code
➕ Insert Code
const cars3 = cars.map((car) =>
  car.isDiesel ? { brand: "Tesla", price: 25000, isDiesel: false } : car);
Feel free to modify the README.md file according to your needs.
