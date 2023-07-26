class Cart:
    def __init__(self):
        self.__products = []  # Список товаров в корзине

    def add_product(self, product):
        self.__products.append(product)

    def calculate_total_cost(self):
        total_cost = 0
        for product in self.__products:
            total_cost += product.cost
        return total_cost
        
# Создание экземпляра корзины
cart = Cart()

# Создание экземпляров товаров
product1 = Product("Футболка", "одежда", 50)
product2 = Product("Кроссовки", "обувь", 80)
product3 = Product("Серьги", "украшение", 30)

# Добавление товаров в корзину
cart.add_product(product1)
cart.add_product(product2)
cart.add_product(product3)

# Подсчет общей стоимости товаров в корзине
total_cost = cart.calculate_total_cost()
print("Общая стоимость товаров:", total_cost)
