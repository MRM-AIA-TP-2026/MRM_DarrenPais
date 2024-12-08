cmake_minimum_required(VERSION 3.8)
project(cashier_system)

# Ensure that necessary dependencies are found
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

# Generate interfaces for messages and services
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/Bill.msg"
  "srv/UpdateParams.srv"
  DEPENDENCIES std_msgs
)

# Add executables for nodes
add_executable(bill_publisher src/bill_publisher.cpp)
ament_target_dependencies(bill_publisher rclcpp std_msgs cashier_system_interfaces)

add_executable(bill_subscriber src/bill_subscriber.cpp)
ament_target_dependencies(bill_subscriber rclcpp std_msgs cashier_system_interfaces)

add_executable(parameter_service src/parameter_service.cpp)
ament_target_dependencies(parameter_service rclcpp cashier_system_interfaces)

add_executable(printer src/printer.cpp)
ament_target_dependencies(printer rclcpp cashier_system_interfaces)

# Install targets
install(TARGETS
  bill_publisher
  bill_subscriber
  parameter_service
  printer
  DESTINATION lib/${PROJECT_NAME}
)

# Install generated interfaces
install(DIRECTORY
  msg
  srv
  DESTINATION share/${PROJECT_NAME}
)

ament_package()
