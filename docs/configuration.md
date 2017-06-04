# PipeScript

PipeScript is a language that defines how data retrieval, transformation and loading is coordinated and executed. All pipe scripts are persisted in the [HOCON](https://github.com/typesafehub/config/blob/master/HOCON.md) format and are composed of the following sections:

## System & Operation Definitions
* Global Config
* System Endpoints for Config, Events, Instructions

## Task Definitions

* Functional Operations on the Data Stream

## Pipeline Definitions

* Flow Control between Tasks and other Pipelines

## Service Definition

* Define Bind Points to - URI and Adjectives to a pipeline. The return value from the call is the output of the pipeline.

## Schedule

* Define a default pipeline to start associated with the specific Config.
* Define Active scheduled pipelines 
* Define Active Services

