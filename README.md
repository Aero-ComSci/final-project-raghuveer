# 🌞 Summer Bucket List Tracker  

## 🎯 About This Project  
This program is designed for anyone looking to **track their summer bucket list** in a fun and interactive way! Instead of keeping a written checklist, this Python script automates the process by allowing users to mark activities as completed dynamically.  

## 🔥 Features  
- ✅ Displays a **list of activities** to complete  
- ✅ Allows users to **remove completed activities** from the list  
- ✅ Runs until all activities are completed or the user exits  
- ✅ Provides **real-time updates** on remaining activities  

---

## 🚀 How It Works  
1️⃣ Users start with a **predefined bucket list** of activities.  
2️⃣ The program **displays the list** to the user.  
3️⃣ The user **enters the number** of the activity they’ve completed, and it’s removed.  
4️⃣ The updated list is displayed until all activities are completed or the user exits.  

---

## 📸 Screenshots / Demo  
![image](https://github.com/user-attachments/assets/36591e1e-457d-4b3a-ad8d-8d33bd5b202d)
 
📽️ **Demo Video:** [Watch Here](https://your-video-link-here.com)  

---

## 📝 Code Example  

```python
## Function to display the bucket list
def show_list(activities):
    print("\nSummer Bucket List:")
    for activity in activities:
        print("-", activity)

## List of summer activities
bucket_list = ["Go to the beach", "Go to a different country", "Watch a sunset", 
               "Get Ice Cream", "Go on a road trip", "Have a water fight", "Host a party"]

show_list(bucket_list)

## Loop to track completed activities
while bucket_list:
    done = input("\nEnter the number of an activity you completed (or 'exit' to stop): ")
    if done.lower() == 'exit':
        break
    try:
        done = int(done)
        if 1 <= done <= len(bucket_list):
            activity = bucket_list.pop(done - 1)  
            print(f"Nice! You did: {activity}")  
            show_list(bucket_list)
        else:
            print("Out of Index. Try again!")
    except ValueError:
        print("Please enter a valid number.")

show_list(bucket_list)
print("Enjoy your summer!")
