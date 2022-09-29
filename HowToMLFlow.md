# HowTo MLFlow

This is a tutorial on how to make a quick pipeline and get it up and running.

What we are gonna do in this tutorial is to download a dataset and then log it as an artifact.

Afterwards we are gonna read it from another step and then print the first 10 lines.

## SETUP

To get started you will need 2 things.

1. **Anaconda installed** (used to install python and libraries), you can find the guide on how to install: [here](https://www.datacamp.com/tutorial/installing-anaconda-windows)
2. **MLFlow installed.** The easiest way to install MLFlow is searching for: Anaconda Prompt (Anaconda3) , then clicking enter and making sure the Anaconda Prompt is open, after that you can simply use this pip command to install MLFlow into your Anaconda Environment: pip install mlflow

## CREATING THE PIPELINE

### What does a pipeline consist of?

A pipeline consists of the **steps**, a **conda environment** file/or already made environment and in most cases an **MLPROJECT file**.

The **steps** are what is actually run in the pipeline

The **conda environment** is what determines what packages the pipeline should use (i.e. if you use pandas to read a .csv file, then you would need to have Pandas in your python environment). You can use a conda environment file, or your own local one. To learn more about environment files click [here](https://blog.devgenius.io/using-conda-environments-for-python-all-you-need-to-know-2eb36e224d1c)

The **MLPROJECT file**, this file is kind of like the description of the pipeline and it helps MLFlow understand how your pipeline is run and how to show the runs in the UI

### Creating the steps

To create the steps you of course need to create the python files for the pipeline to use. In this case let's create 3 steps, called each: main.py, data_ingestion.py, data_display.py.

Now that you have created these 3 steps, it's time to make the main.py useful by making it the orchestrator/controller of the 2 other steps execution.

Using the mlflow.run() method allows main.py to execute the other steps.

But mlflow also has to run itself

It would look like this code wise:

```python
data_ingestion_run = mlflow.run(
            "",
            "data_ingestion.py",
            parameters={},
            env_manager="local",
        )

data_display_run = mlflow.run(
            "",
            "data_display.py",
            parameters={},
            env_manager="local",
        )
```

## RUNNING THE PIPELINE

There are a lot of different parameters used in the command used to run the pipeline, I will explain some of the more important ones:

### **Project URI**

The project uri is used to identify where the project you are trying to run is located, there are some specific things you can do with the project uri as well.

The options for what the project uri can be is

- Local URI
- Github URI
- Git over SSH URI

In this tutorial's case we will focus only on local running. To learn more about how the different parameters works and what's allowed go to MLFlows [Documentation](https://mlflow.org/docs/latest/projects.html#running-projects)

#### Local

The Local URI is just the folder path to the pipeline from where you are executing the run command from. This means if you are running the pipeline from the project root folder, then it's the path from the root folder to the pipeline

### **Project version**

This is for Git-based projects. You can use the commit hash or branch name of the Git repository to specify which version you wanna run

### **Entry Point**

You can choose to specify a specific step to start the pipeline on or just leave it empty. (The default is main. So if you wanted to write that just leave it out). This is especially useful if you have a step that faills and want to figure out how many of the other steps would fail as well.

### **Parameters**

They are something you use for different purposes and it’s a longer paragraf just to explain what they are and how to specify them. It’s useful for passing settings you might want to enable or disable through, e.g enabling error detection (if it’s setup)

### **Deployment Mode**

This is used to specify where the run is executed, you run it from a local machine yes, but in many cases you would just use the local machine to queue a run on Databricks or a similar cluster or computing infrastructure.

### **Environment**

This is used to force MLFlow to use another environment than the one that was specified in the mlprojects file. There are uses for this but I have not yet needed to use this for the overall run command (I use the code version of environment specification when starting a step)

## Actually running the pipeline

Now, onto running the project itself. The prefix command for running a project is: mlflow run
Note: When talking about a command it is generally understood that you are using a console/terminal that already is using a environment with mlflow
So an example command could look like this:

```yml
mlflow run iris-pipeline
```

Here is an empty command template:

```yml
mlflow run [project uri] [entry point] [paremeters] [deployment mode] [environment]
```

As you can see, a lot of the different parameters (in the command itself) can be omitted since they might not always be needed. This is where it can differ a whole lot from other projects as well

### RUNNING THE UI

The UI is extremely easy to run since it’s a single command to start the UI. Afterwards it’s more about understanding how to navigate the UI and I’ll give a quick overview after giving the command.
The command for running the UI is:

```yml
mlflow ui
```

Here is a picture explaning some of the UI
![alt text](UIshowcase.png)