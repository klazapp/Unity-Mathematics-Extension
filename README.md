# Klazapp Mathematics Package

## Introduction

The Klazapp Mathematics Package enhances mathematical operations in Unity with a set of utility functions designed to simplify common calculations, particularly those not included in the Unity Math library or requiring specific behaviors like clamping values in unique ways or handling colors and vectors more efficiently.

## Features

- **Extended Math Operations:** Functions for angles, approximations, and clamping beyond Unity's standard math library.
- **Color Interpolation:** Custom methods to interpolate between two colors accurately.
- **Vector Operations:** Enhanced vector calculations to handle various types of data including new struct types like `decimal2`.

## Dependencies

- Unity 2020.1 or later
- Unity.Mathematics package

## Compatibility

| Compatibility | URP | BRP | HDRP |
|---------------|-----|-----|------|
| Supported     | Yes | Yes | Yes  |

## Installation

Download the package and import it into your Unity project. Ensure that the Unity.Mathematics package is already installed in your project.

## Usage

Certainly! Here's an enhanced "Usage" section for your README, including sample code snippets that demonstrate how to utilize the functions in the `mathExtension` class from your mathematics package.

---

## Usage

Include the package in your script by adding `using com.Klazapp.Utility;`. Below are examples of how to use the extended math functions provided by the `mathExtension` class.

### Angle Between Vectors

Calculate the angle between two vectors:

```csharp
float3 from = new float3(1, 0, 0);
float3 to = new float3(0, 1, 0);
float angle = mathExtension.angle(from, to);
Debug.Log("Angle in degrees: " + angle);
```

### Color Interpolation

Lerp between two colors:

```csharp
Color startColor = Color.red;
Color endColor = Color.blue;
float progress = 0.5f; // Midway
Color resultColor = mathExtension.lerp(startColor, endColor, progress);
Debug.Log("Interpolated Color: " + resultColor);
```

### Clamp Integer Values

Clamp an integer value to ensure it is above a minimum threshold:

```csharp
int value = 5;
int minValue = 10;
int clampedValue = mathExtension.clampToAboveValue(value, minValue);
Debug.Log("Clamped Value: " + clampedValue);
```

### Using `decimal2`

Create a `decimal2` structure and perform operations:

```csharp
decimal2 point1 = new decimal2(1.5m, 2.5m);
decimal2 point2 = new decimal2(3.5m, 4.5m);
decimal2 sum = point1 + point2;
Debug.Log("Sum of decimal2 points: " + sum);
```

These examples provide a straightforward way to leverage the additional mathematical functionalities provided by the Klazapp Mathematics Package in your Unity projects.

## To-Do List

- [ ] Add more complex mathematical operations such as matrix solvers.
- [ ] Introduce more geometric functions.
- [ ] Expand compatibility to more Unity versions and additional rendering pipelines.

## License

Distributed under the MIT License. See `LICENSE` for more information.
