import re
import random

# Base Class
class Participant:
    def __init__(self, name):
        self.name = name
        self.hand = []
        self.score = 0

    def add_card(self, card):
        self.hand.append(card)
        # Add logic here to update score
        
# Inheritance for 'Complete' score
class Player(Participant):
    def __init__(self, name, balance=100):
        super().__init__(name)
        self.balance = balance

class Dealer(Participant):
    def __init__(self):
        super().__init__("Dealer")
