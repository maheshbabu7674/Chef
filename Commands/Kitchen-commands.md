Test Kitchen is a tool designed to make it easy to test infrastructure code on one or more platforms. Below are some common `kitchen` commands along with examples:

### 1. Creating and Managing Instances:

- **Create a New Test Instance:**
  ```bash
  kitchen create
  ```
  This command creates a new virtual machine or container instance based on the configuration specified in your `.kitchen.yml` file.

- **List Available Platforms:**
  ```bash
  kitchen list
  ```
  Lists all the available instances defined in your `.kitchen.yml` file along with their status.

- **Destroy an Instance:**
  ```bash
  kitchen destroy
  ```
  Destroys the current test instance.

### 2. Converging and Verifying:

- **Converge an Instance:**
  ```bash
  kitchen converge
  ```
  Converges the current test instance, applying your cookbook and configuring the system.

- **Reconverge an Instance:**
  ```bash
  kitchen converge
  ```
  Useful after making changes to your cookbook. It destroys the existing instance and creates a new one before converging.

- **Run InSpec Tests:**
  ```bash
  kitchen verify
  ```
  Runs InSpec tests on the converged instance to verify its state.

### 3. Testing:

- **Run All Test Stages (create, converge, verify, destroy):**
  ```bash
  kitchen test
  ```
  This command performs the complete test lifecycle: create, converge, verify, and destroy.

- **Run a Specific Suite:**
  ```bash
  kitchen test -s suite_name
  ```
  Targets a specific suite for testing if your `.kitchen.yml` file defines multiple suites.

- **Run on a Specific Platform:**
  ```bash
  kitchen test -p platform_name
  ```
  Chooses a specific platform for testing if your `.kitchen.yml` file defines multiple platforms.

### 4. Other Utility Commands:

- **Login to an Instance:**
  ```bash
  kitchen login
  ```
  Logs into the test instance using SSH.

- **Show Configuration:**
  ```bash
  kitchen diagnose --all
  ```
  Displays detailed information about the Test Kitchen configuration and environment.

These commands help you manage the testing lifecycle of your infrastructure code using Test Kitchen. Adjust the options based on your specific use case and configuration in the `.kitchen.yml` file.
