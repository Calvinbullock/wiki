
# Metrics
Design metrics for programming as coined by Professor Helfitch (one of my BYU-I professors)

## Efficiency
- ...
    - O(1)        Constant    Performance is unrelated to the amount of input into the algorithm
    - O(log n)    Logarithmic Performance is a log of the amount of input into the algorithm
    - O(n)        Linear      Performance is directly related to amount of input into the algorithm
    - O(n log n)  N-Log-N     Performance is linear times logarithmic
    - O(n2)       N-Squared   Performance is the square of the amount of input into the algorithm
    - O(2n)       2-to-the-N  Performance is really bad

## Maintainability
- Perfective Maintenance
    - Improvements and enhancements that do not change initial functionality.
        For example, performance improvements would be perfective. On average,
        this constitutes 5% of maintenance costs.
- Corrective Maintenance
    - Fixing defects in the software that were discovered after it was initially deployed.
        This is usually about 17% of maintenance costs.
- Adaptive Maintenance
    - Adjusting software so it can continue to function as before in a new or changing environment.
        This is usually 18% of costs.
- Enhancements
    - Adding new functionality that was not part of the initial specification or design. This is usually 60% of costs.

## Cohesion
- Cohesion - if each function is focused on a single task.
    - Strong - The function performs one task completely.
    - Extraneous - There exists extra functionality.
    - Partial - The function does not complete a single task.
    - Weak- Both extraneous and partial.

## Coupling
- Coupling -  complexity of the interface between units of software,
    - Trivial - No information interchange exists.
    - Encapsulated - Parameters are convenient and always valid.
    - Simple - Parameters are easy to select and interpret.
    - Complex - At least one parameter is difficult.
    - Document - A rich language is utilized.
    - Interactive - Nontrivial dialog.
    - Superfluous - Any unnecessary parameter.

## Convenience
- Convenience - how easy it is for a client to use a class in an application (code / class / function).
    - Seamless - Perfectly aligned with the needs of the application.
    - Easy - No extra work is required to manipulate.
    - Straightforward - Any data manipulation can be readily performed.
    - Convoluted - Much needs to be done to use the class.
    - Prohibitive - More work is required than it is worth.

## Fidelity
- Fidelity - suitability of a class in representing a design concern
    - Complete - States of the class completely match the design concern.
    - Extraneous - There are extra states but none missing.
    - Partial - There are missing states but nothing extra.
    - Poor - The class poorly represents the design concern.

## Abstraction
- Abstraction - shielding users from unnecessary implementation details.
    - Complete - No implementation details are revealed to the client.
    - Opaque - Unimportant implementation details are revealed to the client.
    - Porous - Knowledge of implementation are very helpful to the client.
    - Critical - The client must deeply understand the implementation details.

## Robustness
- Robustness - (TESTING) degree of resistance a class has from being placed in an invalid state or sending invalid data to the client
    - Proven - The design was formally proven to be robust.
    - Resilient - Thoroughly white box tested.
    - Strong - Rigorously and systematically black box tested.
    - Tested - Ad hoc black box tested.
    - Fragile - Only tested in very restricted circumstances.

## Adaptability
- Adaptability - suitability of a base class to leverage existing code to represent previously unknown design concerns through the addition of child classes.
    - Enabling - Much functionality can be added through small changes.
    - Straightforward - Changes can be made solely by adding child classes.
    - Convoluted - Changes require minor alterations to the base class.
    - Prohibitive - The amount of work is greater than the benefit received.
    - Closed - Enhancements through inheritance are not possible.

## Alignment
- Alignment - degree to which the inheritance tree models relationships in the problem domain.
    - Complete - The problem domain and the inheritance tree match.
    - Extraneous - Some classes in the inheritance tree do not match the problem.
    - Partial - There are missing constructs but nothing extra.
    - Poor - The inheritance tree poorly represents the design concern.

## Redundancy
- Redundancy - when common elements exist in an inheritance tree.
    - Distinct - There are no duplicated attributes or operations.
    - Minor - Any duplication exists in non-adjacent classes.
    - Critical - Siblings have duplicate attributes or operations.
    - Redundant - Multiple instances of redundancy exist in the tree.

## malubility
- malubility
