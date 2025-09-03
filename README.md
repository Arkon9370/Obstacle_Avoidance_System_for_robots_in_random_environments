Obstacle Avoidance System for Robots
====================================

An obstacle avoidance system is a critical part of robotic navigation, where a robot must detect obstacles in its path and take appropriate action to avoid collisions. This system uses sensors, such as cameras or LiDAR, to perceive the environment and uses algorithms to make decisions about how to navigate safely. In this project, we will implement a simple obstacle avoidance system for a robot using a reactive control approach. The robot will detect obstacles in its environment and change its trajectory to avoid them.

Methodology
-----------
    
*   **Inputs**: The system takes readings from three front-facing sensors (left, front, and right) as inputs. Each input distance is categorized into three linguistic variables: 'low', 'medium', and 'high'.
        
*   **Outputs**: The controller produces two outputs: the speed for the left wheel and the speed for the right wheel. The wheel speeds are categorized into 'slow', 'medium', and 'fast'.
        
*   **Rules**: A set of fuzzy rules determines the robot's behavior. For example, if the front sensor detects an obstacle at a 'low' distance, the robot might turn right by setting the left wheel to 'fast' and the right wheel to 'slow'. The complete rule base is designed to handle various obstacle configurations.
        

Environment and Tools
---------------------
    
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
        
1.  **Execute the Python Code**:
    
    *   Open and run the code.ipynb Jupyter Notebook.
