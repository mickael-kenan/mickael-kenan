---
layout: post
title: "DDD: Value Objects in Domain-Driven Design: What They Are and How to Use Them"
category: ddd
---
Alright, let's talk about Value Objects in Domain-Driven Design (DDD). I'm still learning about this topic, but I want to share what I've learned so far. Value Objects are one of the core building blocks in DDD, and they can be super useful in organizing our code and making it more expressive.

<!--more-->

In a nutshell, Value Objects are small, immutable objects that represent a concept in our domain. They don't have an identity, meaning that two Value Objects are considered equal if their properties are equal.

Let's dive in a bit deeper with an example. Suppose we're building an online store, and we need to handle money. Instead of using primitive types like numbers or strings for money, we can create a `Money` Value Object that has properties like `amount` and `currency`. This way, our code will be more readable and less error-prone.

Here's a simple `Money` Value Object in TypeScript:

```typescript
class Money {
  readonly amount: number;
  readonly currency: string;

  constructor(amount: number, currency: string) {
    this.amount = amount;
    this.currency = currency;
  }

  equals(other: Money): boolean {
    return this.amount === other.amount && this.currency === other.currency;
  }
}
```

In this example, the `Money` class has two properties: `amount` and `currency`. The `equals` method checks if two `Money` objects are equal by comparing their properties.

Now, let's see how we can use this `Money` Value Object in our online store.

Imagine we need to calculate the total price of an order. Instead of dealing with primitive numbers and strings, we can work with `Money` objects, making our code more expressive and less prone to errors.

Here's an example of how we can calculate the total price of an order:

```typescript
class Order {
  private items: Array<{ price: Money; quantity: number }>;

  constructor(items: Array<{ price: Money; quantity: number }>) {
    this.items = items;
  }

  getTotalPrice(): Money {
    let totalAmount = 0;
    let currency = "";

    for (const item of this.items) {
      totalAmount += item.price.amount * item.quantity;
      currency = item.price.currency;
    }

    return new Money(totalAmount, currency);
  }
}
```

In the `Order` class, we store an array of items, each with a `price` (a `Money` object) and `quantity`. To calculate the total price of the order, we iterate through the items, multiply the item's price by its quantity, and sum up the amounts.

Notice how using the `Money` Value Object makes the code more expressive and easier to understand. We can now see that we're working with money and not just some random numbers.

Value Objects are a powerful concept in DDD, and they can help us write cleaner, more expressive, and less error-prone code. I hope this explanation has been helpful for you. Remember, I'm still learning, so there might be more to it than what I've shared here. But for now, I hope you find this useful in your own projects!