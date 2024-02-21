# Define classes and functions for the loyalty program app

class Customer:
    def __init__(self, name, email):
        self.name = name
        self.email = email
        self.points = 0

    def earn_points(self, amount):
        self.points += amount

    def redeem_points(self, reward):
        # Logic to redeem points for rewards
        pass

class Reward:
    def __init__(self, name, points_required):
        self.name = name
        self.points_required = points_required

class LoyaltyProgramApp:
    def __init__(self):
        self.customers = []
        self.rewards = []

    def add_customer(self, name, email):
        customer = Customer(name, email)
        self.customers.append(customer)

    def add_reward(self, name, points_required):
        reward = Reward(name, points_required)
        self.rewards.append(reward)

    def make_purchase(self, customer_email, purchase_amount):
        # Update customer's points based on purchase amount
        pass

    def redeem_reward(self, customer_email, reward_name):
        # Redeem reward for customer if they have enough points
        pass

# Example usage of the LoyaltyProgramApp class

app = LoyaltyProgramApp()

# Add customers
app.add_customer("Alice", "alice@example.com")
app.add_customer("Bob", "bob@example.com")

# Add rewards
app.add_reward("Free Coffee", 50)
app.add_reward("50% Off", 100)

# Simulate purchases and point earning
app.make_purchase("alice@example.com", 20)
app.make_purchase("bob@example.com", 30)

# Simulate reward redemption
app.redeem_reward("alice@example.com", "Free Coffee")
