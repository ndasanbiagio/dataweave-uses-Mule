# MuleSoft DataWeave Examples

## Overview

This project demonstrates various DataWeave 2.0 transformations using MuleSoft flows. The transformations cover a range of functions, including basic mathematical operations, string manipulations, filtering, and array processing. These examples are designed to showcase the flexibility and power of DataWeave in handling different data transformation requirements.

## Flows

### 1. `lambdaExpressionFlow`

#### Description

The `lambdaExpressionFlow` demonstrates the usage of lambda expressions in DataWeave for various operations, including mapping, filtering, and basic function implementation.

#### Transformations

- **firstExpression**:
  - **Purpose**: Transforms payload data using a lambda function to map fields to a new JSON structure.
  - **Example**:
    ```json
    {
      "firstName": "John",
      "lastName": "Doe",
      "enterpriseName": "Acme Corp"
    }
    ```

- **lambdaOnArray**:
  - **Purpose**: Demonstrates the use of lambda expressions on arrays to modify the casing of strings.
  - **Example**:
    ```json
    {
      "EmployeeName": ["MULE", "SOFT", "SALESFORCES"],
      "EmployeeName": ["mule", "soft", "salesforces"]
    }
    ```

- **basicExample**:
  - **Purpose**: Shows basic lambda usage with operations and typecasting.
  - **Example**:
    ```json
    {
      "key1": "5",
      "key2": 5
    }
    ```

- **implementFilterLambda**:
  - **Purpose**: Demonstrates filtering an array of numbers using lambda expressions.
  - **Example**:
    ```json
    [5, 6]
    ```

### 2. `dwFlow`

#### Description

The `dwFlow` showcases various DataWeave operations on arrays, including counting, dividing, slicing, and summing elements.

#### Transformations

- **countBy**:
  - **Purpose**: Counts elements in an array based on a condition (modulus operation).
  - **Example**:
    ```json
    {
      "countBy": [true, false, true, false, true, false]
    }
    ```

- **divideBy**:
  - **Purpose**: Divides elements in an array by a specified number.
  - **Example**:
    ```json
    {
      "divideBy": [0, 1, 1, 2, 2, 3],
      "divideBy3": [0, 0, 1, 1, 2, 2],
      "divideBy4": [0, 0, 0, 1, 1, 1]
    }
    ```

- **indexOf**:
  - **Purpose**: Finds the index of a specified element in an array.
  - **Example**:
    ```json
    1
    ```

- **slice**:
  - **Purpose**: Slices an array from a specified start to end index.
  - **Example**:
    ```json
    [2, 3, 4]
    ```

- **sumBy**:
  - **Purpose**: Sums values of a specified key in an array of objects.
  - **Example**:
    ```json
    {
      "sumby": 60
    }
    ```

### 3. `dwFlow1`

#### Description

The `dwFlow1` illustrates more complex DataWeave operations, such as concatenating arrays, calculating averages, and finding distinct elements.

#### Transformations

- **++--**:
  - **Purpose**: Demonstrates concatenation and subtraction of arrays, along with string concatenation.
  - **Example**:
    ```json
    {
      "conNumbers": [1, 2, 3, 4, 5, 6, "a"],
      "UnconNumbers": [2, 3],
      "payload1": "Hi Mule!!!"
    }
    ```

- **Average**:
  - **Purpose**: Calculates the average of numbers in an array.
  - **Example**:
    ```json
    {
      "avg1": 500.5,
      "avg2": 2230
    }
    ```

- **distinctBy**:
  - **Purpose**: Finds distinct elements in an array based on a specified condition.
  - **Example**:
    ```json
    [
      {
        "removeDuplicateElements": 0
      },
      {
        "removeDuplicateElements": 1
      },
      ...
    ]
    ```

### 4. `dwFlow2`

#### Description

The `dwFlow2` provides examples of DataWeave functions for string and array manipulation, such as finding indexes, checking for blanks, and flattening arrays.

#### Transformations

- **indexOf**:
  - **Purpose**: Finds the index of a character in a string or element in an array.
  - **Example**:
    ```json
    {
      "key1": 0,
      "key2": 3
    }
    ```

- **isUsage**:
  - **Purpose**: Demonstrates the use of `isBlank`, `isDecimal`, and `isEmpty` functions.
  - **Example**:
    ```json
    {
      "insblanks": {
        "isBlank1": true,
        "isBlank2": false,
        "isBlank3": true
      },
      "isdecimals": {
        "isdecimal1": true,
        "isdecimal2": false
      },
      ...
    }
    ```

- **minAndMax**:
  - **Purpose**: Calculates the minimum and maximum values in an array.
  - **Example**:
    ```json
    {
      "max": {
        "maximun": 2222222
      },
      "min": {
        "minimun": 0
      }
    }
    ```

- **mod**:
  - **Purpose**: Applies modulus operations on an array of numbers.
  - **Example**:
    ```json
    [1, 0, 0, 0]
    ```

- **Flatten**:
  - **Purpose**: Flattens a nested array and extracts specific fields from nested objects.
  - **Example**:
    ```json
    {
      "key1": [
        {
          "semester": "1",
          "yearofpassing": "2024"
        },
        ...
      ],
      "key2": ["Mulesoft", "SalesForces"]
    }
    ```

## Getting Started

1. **Prerequisites**:
   - MuleSoft Anypoint Studio
   - Basic knowledge of DataWeave 2.0

2. **Importing the Project**:
   - Clone the repository or download the project zip.
   - Open Anypoint Studio and import the project.

3. **Running the Flows**:
   - Deploy the Mule application.
   - Trigger the flows to see the transformations in action.
