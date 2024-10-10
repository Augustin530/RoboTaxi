class RoboTaxi:
    def __init__(self, location, destination):
        self.location = location  # 當前位置
        self.destination = destination  # 目的地
        self.passengers = 0
        self.autonomous_mode = True  # 自動駕駛模式

    def pickup_passenger(self, num_passengers):
        self.passengers += num_passengers
        print(f"Picked up {num_passengers} passengers.")

    def drive(self):
        if self.autonomous_mode:
            print(f"Driving autonomously from {self.location} to {self.destination}.")
        else:
            print(f"Manual driving from {self.location} to {self.destination}.")
    
    def dropoff_passenger(self):
        print(f"Dropped off {self.passengers} passengers at {self.destination}.")
        self.passengers = 0

    def switch_to_manual(self):
        self.autonomous_mode = False
        print("Switched to manual driving mode.")

    def switch_to_autonomous(self):
        self.autonomous_mode = True
        print("Switched to autonomous driving mode.")

# 模擬 Robotaxi 操作
taxi = RoboTaxi("Central Park", "Times Square")
taxi.pickup_passenger(2)
taxi.drive()
taxi.dropoff_passenger()
taxi.switch_to_manual()
taxi.drive()
# RoboTaxi
