# FitnessAppModule Library

The FitnessAppModule Library is a C# library that provides classes and functionality for managing user exercises and their history within a fitness application.

## User

The `User` class represents a user in the fitness application. It has the following properties:

- `Name`: The name of the user.
- `UserID`: The ID of the user.
- `UserExerciseList`: A list of exercises associated with the user.
- `UserHistoryOfExerciseList`: A list of exercise history records for the user.

## Exercise

The `Exercise` class is an abstract base class for different types of exercises. It has the following properties:

- `Name`: The name of the exercise.
- `Description`: A description of the exercise.
- `MinReps`: The minimum number of repetitions for the exercise.
- `MaxReps`: The maximum number of repetitions for the exercise.
- `HistoryOfExercise`: An instance of the `HistoryOfExercise` class representing the exercise history.

## HistoryOfExercise

The `HistoryOfExercise` class represents the history of an exercise. It can be associated with an exercise to track its progress over time.

## Push

The `Push` class is a derived class of `Exercise` representing push exercises. It has the same properties as the base class.

## Pull

The `Pull` class is a derived class of `Exercise` representing pull exercises. It has the same properties as the base class.

## Legs

The `Legs` class is a derived class of `Exercise` representing leg exercises. It has the same properties as the base class.

## Main

The `Main` class contains examples of different push and pull exercises. Each exercise is instantiated with its name, description, minimum and maximum repetitions, and a history object. Here are some examples:

- `BenchPress`: The traditional bench press exercise.
- `IndependentBenchPress`: The independent bench press machine exercise.
- `InclineBenchPress`: The incline bench press exercise.
- `DeclineBenchPress`: The decline bench press exercise.
- `Dips`: The dips bodyweight exercise.
- `MilitaryPress`: The military press exercise.
- `OHP`: The overhead press exercise.
- `ChestFlys`: The chest flys exercise.

Each exercise has a detailed description on how to perform it correctly and safely.

## Usage

To use the FitnessAppModule Library, you can include the namespace `FitnessAppModule_Library` in your C# code and create instances of the classes described above.

```csharp
using FitnessAppModule_Library;

// Example usage
User user = new User
{
    Name = "John Doe",
    UserID = 1,
    UserExerciseList = new List<Exercise>(),
    UserHistoryOfExerciseList = new List<HistoryOfExercise>()
};

Exercise benchPress = new Push
{
    Name = "Bench Press",
    Description = "The bench press is a compound exercise...",
    MinReps = 6,
    MaxReps = 12,
    HistoryOfExercise = new HistoryOfExercise()
};

user.UserExerciseList.Add(benchPress);
```

Feel free to explore the library and use it to enhance your fitness application!

**Note:** This is a simplified version of the code provided, and it assumes that the necessary dependencies and proper class instantiation are handled correctly in your application.
