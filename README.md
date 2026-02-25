# Vanilla Option Pricing - Binomial Model
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Project developed for the "Mathematical Finance" course at Università di Verona.**

## Project Overview
This Java project is designed for the pricing of **Vanilla Options** (Call and Put), covering both **European** and **American** styles, utilizing the Binomial Options Pricing Model (Cox-Ross-Rubinstein).

The software adheres to Object-Oriented Programming (OOP) principles to ensure modularity and extensibility. Key functionalities include the calculation of risk-neutral probabilities, the generation of the underlying asset price tree, and option valuation via *backward induction*.


## Key Features
* **Flexible Binomial Model**: Full parameterization (volatility, risk-free rate, time steps, horizon).
* **European Option Pricing**: Standard valuation at maturity.
* **American Option Pricing**: Support for early exercise evaluation (Snell Envelope).
* **Black-Scholes Comparison**: Validation of discrete model convergence against the continuous Black-Scholes formula.
* **Input validation**: Ensure the underlying model's simulation horizon covers the option's full time to maturity
* **Visualization**: Console output of price trees and probability matrices.

## Project Structure
The project follows the standard Maven directory structure and is organized into the following packages:

* `it.univr.binomialmodeltrees`: Contains the stochastic model logic (`BinomialModel`) for the underlying asset evolution.
* `it.univr.options`: Defines the `Options` interface and concrete implementations (`EuropeanOption`, `AmericanOption`).
* `it.univr.utilities`: Utility methods for array manipulation and matrix operations.

## Tech Stack
* **Java 17**
* **Maven**: Dependency management and build automation
* **Finmath Lib**: Library for advanced financial algorithms

## How to Run
The project includes a demo class that performs a full simulation, printing the trees and comparing prices.

1.  Clone the repository.
2.  Run the `BinomialModelTest` class located in `src/test/java/it/univr/binomialmodeltest/`.

The output will display:
1.  The underlying asset price tree.
2.  The probability matrix.
3.  Calculated prices for European and American Call/Put options.
4.  Comparison with the theoretical Black-Scholes price.

### Example Output
```text
All realizations for all times are:
t=0: 100,0000000000000 
t=1: 106,6678614786084 93,7489498840796 
...

Comparison of the European and American Put prices
European Put Option price: 6.042226351743356
American Put Option price: 6.463389706267749
```

## Authors & Acknowledgments

**Development Team:**
* Lorenzo Visonà Dalla Pozza
* Alberto Oliva Medin

**Credits:**
* This project is based on a template provided by **Prof. Alessandro Gnoatto**, specifically regarding the base structure of the `BinomialModel` class.
* The implementation of **European and American Options** (including Snell Envelope logic), input validation and the pricing architecture was developed by the team as part of the project work.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
