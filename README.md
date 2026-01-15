# Hands on ML for AIPMs

This exercise is designed for Project Management students to explore **how machine learning models can inform product decisions**. You are a PM at XYZ, a subscription-based SaaS platform, and your goal is to **predict which users are likely to churn** in the next 30 days. 

Using behavioral and subscription data, you will build simple ML models (logistic regression, KNN, and decision trees) to forecast churn, evaluate their performance, and make **business trade-offs**. The exercise emphasizes:

- Understanding **features in a business context**  
- Evaluating models with metrics like recall, precision, and F1  
- Considering **product constraints**, explainability, and risk  
- Practicing **bias–variance trade-offs** from a PM perspective  

> This is a small, illustrative dataset intended to focus on **decision-making and product reasoning**, not production-grade modeling.

Please look into the `task.md` file for the detailed description of the [exercise](task.md)

---

## Set up your Environment

The added [requirements file](requirements.txt) contains all libraries and dependencies we need to execute the notebooks.

### **`macOS`** type the following commands : 

- Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
### **`WindowsOS`** type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-Bash` CLI :
    ```
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```


*Note: If there are errors during environment setup, try removing the versions from the failing packages in the requirements file.*
