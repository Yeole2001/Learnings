# Kubernetes Concepts #
--------------

## Imperative and Declrative for Kubectl Commands

* Kubectl have Imperative and Declarative Commands
* Explained with Team Making analogy -

| Concept         | Real-World Tea Example                                                      | Explanation                                                                   |
| --------------- | --------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Imperative**  | You make tea step-by-step yourself:                                         | You control **how** it gets done.                                             |
|                 | 1. Boil water<br>2. Add tea leaves<br>3. Add milk/sugar<br>4. Pour into cup | Every step is explicitly defined.                                             |
| **Declarative** | You tell your mom: “I want a cup of tea.”                                   | You specify **what you want**, not how to do it.                              |
|                 | Mom decides how to prepare it.                                              | The system (mom/Kubernetes) figures out the steps to reach the desired state. |

Imperative = You give instructions: "Do this, then this..."

Declarative = You define the goal: "I want it like this."

## 📦 kubectl Command Comparison

| `kubectl` Command | Mode         | Object Doesn't Exist    | Object Already Exists      | Notes                                        |
|-------------------|--------------|--------------------------|-----------------------------|----------------------------------------------|
| `create`          | Imperative   | Creates object           | ❌ Error                    | Use for new resources only                   |
| `apply`           | Declarative  | Creates object           | Updates with partial config | Smart merge – recommended for most use cases |
| `replace`         | Imperative   | ❌ Error                  | Deletes and recreates       | Risky – must specify full config             |

-------------------------


# Kubernetes Commands #
--------------

* Get all the resources

#kubectl get all

* To get Kubernetes Objects/Resources

#kubectl get pods/namespaces(ns)/nodes

* List recent events in the default namespace

#kubectl events

* To watch on pods
  
#watch “kubectl get pod -A -o wide”




