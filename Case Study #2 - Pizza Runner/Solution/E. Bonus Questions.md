# 🍕 Case Study #2 - Pizza Runner
## E. Bonus Questions
### If Danny wants to expand his range of pizzas - how would this impact the existing data design? Write an INSERT statement to demonstrate what would happen if a new Supreme pizza with all the toppings was added to the Pizza Runner menu?

```TSQL
INSERT INTO pizza_runner.pizza_names (pizza_id, pizza_name)
VALUES (3, 'Farmhouse');

ALTER TABLE pizza_runner.pizza_recipes
ALTER COLUMN toppings VARCHAR(50);

INSERT INTO pizza_runner.pizza_recipes (pizza_id, toppings)
VALUES (3, '1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12');
```

we need to update pizza_recipes as well to update toppings for newly added "Farmhouse" pizza.
