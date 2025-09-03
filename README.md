Obstacle Avoidance System for Robots
====================================

This project implements an obstacle avoidance system for a differential drive robot in a simulated environment using a fuzzy logic controller. The robot is equipped with eight ultrasonic sensors to perceive its surroundings and navigate through an environment with random obstacles without collision.

Methodology
-----------

The core of the navigation system is a Mamdani fuzzy logic controller, which makes decisions based on sensor inputs to control the robot's movement.

*   **Robot and Sensors**: The simulation uses a Pioneer 3-DX robot model equipped with 8 ultrasonic sensors. These sensors provide distance readings from the front, sides, and back of the robot.
    
*   **Fuzzy Logic Controller**:
    
    *   **Inputs**: The system takes readings from three front-facing sensors (left, front, and right) as inputs. Each input distance is categorized into three linguistic variables: 'low', 'medium', and 'high'.
        
    *   **Outputs**: The controller produces two outputs: the speed for the left wheel and the speed for the right wheel. The wheel speeds are categorized into 'slow', 'medium', and 'fast'.
        
    *   **Rules**: A set of fuzzy rules determines the robot's behavior. For example, if the front sensor detects an obstacle at a 'low' distance, the robot might turn right by setting the left wheel to 'fast' and the right wheel to 'slow'. The complete rule base is designed to handle various obstacle configurations.
        

Environment and Tools
---------------------

*   **Simulation Environment**: The project is designed to run in the **CoppeliaSim** (formerly V-REP) robotics simulator.
    
*   **Python Libraries**:
    
    *   numpy: For numerical operations.
        
    *   matplotlib: For plotting and visualization.
        
    *   scikit-fuzzy: For implementing the fuzzy logic controller.
        

Files in this Project
---------------------

*   code.ipynb: A Jupyter Notebook containing the Python code to connect to the CoppeliaSim simulator, define the fuzzy logic controller, and run the obstacle avoidance simulation.
    

Dependencies
------------

You need to install the following Python packages to run the project.

Bash

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pip install numpy  pip install matplotlib  pip install scikit-fuzzy   `

How to Run
----------

1.  **Set up CoppeliaSim**:
    
    *   Download and install CoppeliaSim.
        
    *   Open the simulator and load the appropriate scene file containing the Pioneer 3-DX robot and obstacles.
        
2.  **Run the Simulation**:
    
    *   Start the simulation in CoppeliaSim by pressing the "Play" button.
        
3.  **Execute the Python Code**:
    
    *   Open and run the code.ipynb Jupyter Notebook.
        
    *   The script will connect to the CoppeliaSim remote API, read sensor data, process it through the fuzzy controller, and send motor speed commands back to the robot, enabling it to navigate the environment.