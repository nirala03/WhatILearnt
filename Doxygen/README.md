# Doxygen — Generating C++ Documentation

## Introduction

Doxygen is a documentation-generation utility that extracts information from source files containing specially formatted comments. It can organize descriptions of program elements into documentation that is easier for developers and readers to navigate.

The exercise in this directory uses a small C++ application to demonstrate how documentation can be written and generated systematically.

## Application Overview

The sample project is divided into three principal source files:

| File | Responsibility |
|---|---|
| `Logger.h` | Implements a basic logging facility |
| `CalculationEngine.h` | Contains the mathematical calculation component |
| `main.cpp` | Serves as the program entry point and documentation landing page |

The two main classes have separate responsibilities. The logger handles messages produced during execution, while the calculation engine performs a power operation and uses the logger to report relevant events.

### Logging Component

The `Logger` class defines four severity levels:

- `Debug`
- `Info`
- `Warning`
- `Error`

A minimum severity level can be selected so that messages below the chosen threshold are ignored. The logger formats the remaining messages with a corresponding level label.

### Calculation Component

The `CalculationEngine` class provides a `power()` method that accepts a numerical base and an integer exponent.

Its implementation handles positive and negative exponents and reports exceptional cases through the logging component. In particular, zero raised to a negative exponent is treated as an invalid operation.

The source also contains a TODO concerning the minimum representable integer exponent. Negating that value can overflow, so it remains an edge case worth addressing.

## Documenting the Source

An important part of the exercise is the use of Doxygen comment commands to describe program elements.

The project demonstrates commands such as:

| Annotation | Intended Use |
|---|---|
| `@file` | Supplies information about a source file |
| `@class` | Introduces a class description |
| `@brief` | Gives a concise summary |
| `@details` | Provides additional explanation |
| `@param` | Explains a function argument |
| `@return` | Describes the returned result |
| `@throws` | Identifies possible exceptions |
| `@enum` | Documents an enumeration |
| `@todo` | Records an outstanding task |
| `@mainpage` | Defines the opening page of the documentation |

The assignment requires the documentation to cover the logging class, its log-level enumeration and constructor, the calculation engine, and its `power()` method.

## Configuration

The `Doxyfile` determines how Doxygen processes the project.

The configuration specifies the project name, source inputs, file patterns, output location, extraction settings, and documentation options. It also enables source browsing and warning checks for undocumented elements and documentation errors.

The configured project output directory is `docs`.

## Generating Documentation

Doxygen can be installed on Ubuntu with:

```bash
sudo apt install doxygen
```

Once installed, move to the directory containing the configuration file and execute:

```bash
doxygen Doxyfile
```

The assignment also requires PDF documentation. With the configured output directory, the generated LaTeX files are expected under `docs/latex`. Navigate there and run:

```bash
cd docs/latex
make
```

This requires the relevant LaTeX tools to be installed.

**Configuration detail:** The assignment asks for HTML as well as LaTeX output. The current checked-in configuration sets `GENERATE_HTML = NO` and `GENERATE_LATEX = YES`. To generate both formats using this configuration, the HTML option must be enabled.

## Files Included

The directory contains the assignment instructions and the solution material, including the C++ source files and the Doxygen configuration.

## Takeaway

The exercise illustrates how source code can carry its own documentation and how a tool such as Doxygen can turn that information into a more accessible reference.

It also highlights the importance of documenting interfaces and expected behaviour, not merely describing what individual lines of code do.