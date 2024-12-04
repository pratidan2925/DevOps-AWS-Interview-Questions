#### 8. How do you execute a shell script within a Python script?
Answer: A shell script can be executed within a Python script using the subprocess module. The subprocess.run() function is commonly used to execute shell commands and capture their output.
Example:
python
Copy code
import subprocess

result = subprocess.run(['./script.sh'], capture_output=True, text=True)
print(result.stdout)

Scenario: In a recent automation task, I used Python to execute a shell script that set up the environment for a larger deployment process. This allowed for better integration and control within the Python script.

#### 29. If you’re developing a Python-based application, how do you separate the packages needed for your local deployment to avoid interfering with globally installed packages?
Answer: To isolate packages for a Python-based application:
Virtual Environments: Use venv or virtualenv to create a virtual environment.
Package Management: Use pip to install packages within the virtual environment, preventing conflicts with globally installed packages.
Scenario: I created a virtual environment using python3 -m venv myenv and installed all required packages within it for a Python project, avoiding any interference with the global Python environment.
