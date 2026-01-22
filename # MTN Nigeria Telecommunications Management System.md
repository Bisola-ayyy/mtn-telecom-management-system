# MTN Nigeria Telecommunications Management System  
# SEN 201 Assignment  
# Name: Onifade Rebecca Bisola  
# Matric Number: 24/14619  
  
# ======================================  
# Subscriber Module  
# ======================================  
subscribers = [  
    {"name": "Onifade Rebecca Bisola", "number": "08012345678", "plan": "MTN Data 1GB", "balance": 2500, "data_used": 200},  
    {"name": "Adekunle Samuel", "number": "08087654321", "plan": "MTN Talktime 500", "balance": 500, "data_used": 0},  
    {"name": "Chukwuemeka Blessing", "number": "08011223344", "plan": "MTN Data 2GB", "balance": 4000, "data_used": 1500}  
]  
  
# ======================================  
# Plan Module  
# ======================================  
plans = [  
    {"name": "MTN Data 1GB", "type": "Data", "price": 1000},  
    {"name": "MTN Data 2GB", "type": "Data", "price": 2000},  
    {"name": "MTN Talktime 500", "type": "Talktime", "price": 500},  
    {"name": "MTN Data 5GB", "type": "Data", "price": 4500}  
]  
  
# ======================================  
# Usage Module  
# ======================================  
def display_subscribers():  
    print("\nMTN Subscribers:")  
    for sub in subscribers:  
        print(f"{sub['name']} | Number: {sub['number']} | Plan: {sub['plan']} | Balance: ₦{sub['balance']} | Data Used: {sub['data_used']}MB")  
  
def display_plans():  
    print("\nAvailable MTN Plans:")  
    for plan in plans:  
        print(f"{plan['name']} | Type: {plan['type']} | Price: ₦{plan['price']}")  
  
def check_balance():  
    number = input("\nEnter subscriber number to check balance: ")  
    for sub in subscribers:  
        if sub["number"] == number:  
            print(f"{sub['name']} has a balance of ₦{sub['balance']}")  
            return  
    print("Subscriber not found.")  
  
def check_data_usage():  
    number = input("\nEnter subscriber number to check data usage: ")  
    for sub in subscribers:  
        if sub["number"] == number:  
            print(f"{sub['name']} has used {sub['data_used']}MB of data")  
            return  
    print("Subscriber not found.")  
  
# ======================================  
# Telecom System Module  
# ======================================  
def main_menu():  
    print("\nMTN NIGERIA TELECOMMUNICATIONS MANAGEMENT SYSTEM")  
    print("1. View All Subscribers")  
    print("2. View Available MTN Plans")  
    print("3. Check Subscriber Balance")  
    print("4. Check Data Usage")  
    print("5. Exit")  
  
while True:  
    main_menu()  
    choice = input("\nEnter your choice (1-5): ")  
  
    if choice == "1":  
        display_subscribers()  
    elif choice == "2":  
        display_plans()  
    elif choice == "3":  
        check_balance()  
    elif choice == "4":  
        check_data_usage()  
    elif choice == "5":  
        print("\nThank you for using the MTN Nigeria Telecom System.")  
        break  
    else:  
        print("Invalid choice. Please try again.")  
