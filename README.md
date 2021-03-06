# Toy Robot Simulator

A command line robot simulator is written in Javascript (Node.js).

## Description

* The application is a simulation of a toy robot moving on a square tabletop, of dimensions 5 units x 5 units.
* There are no other obstructions on the table surface.
* The robot is free to roam around the surface of the table, but must be prevented from falling to destruction. Any movement that would result in the robot falling from the table must be prevented, however further valid movement commands must still be allowed.

* The application can read the following commands:

```
PLACE X,Y,F
MOVE
LEFT
RIGHT
REPORT
```
* `PLACE` will put the toy robot on the table in position X,Y and facing NORTH, SOUTH, EAST or WEST.

* `MOVE` will move the toy robot one unit forward in the direction it is currently facing.

* `LEFT` and `RIGHT` will rotate the robot 90 degrees in the specified direction without changing the positon of the robot.

* `REPORT` will announce the X,Y and F of the robot. This can be in any form, but standard output is sufficient.

### Constraints

The toy robot cannot fall off the table during movement. This also includes the initial placement of the toy robot. Any move that would cause the robot to fall will be ignored.

### Input Format

Your file should start with `place` command follows by one space than the position. All the other commands are valid after placing the robot on the table.

The `test.txt` is provided for you. You can also create your own file input.

Your file should look like the following examples:

```
PLACE 0,0,NORTH
MOVE
REPORT
```

```
PLACE 1,2,EAST
MOVE
MOVE
LEFT
MOVE
REPORT
```

### Output Format

After the reading all the commands, `report` will display the result as `Output: x, y, direction`. For example, the result from the above example will output `Output: 0, 1, NORTH` and `Output: 3, 3, NORTH `

The first example, it started at position 0, 0 North. Then just moved one step. The second one moved twice then turned left (North) and another step. Thus, the new position is 3, 3, North.

### Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

This project was built using `Node.JS version 8.6.0`. You need to have version 8 and above in order to run it. It was developed and tested using `Ubuntu 16.04.3 LTS 64-bit` 

You will need the following dependency for testing:

```
Mocha
```

### Installing

`cd Toy_Robot_Simulator && npm install`

## Running the tests

After installing the project, run `npm start [myInstruction.txt]`

`e.g: npm start instruction.txt`

To run the test, run `npm test` and it will run everything. Should fail one test for incorrect text file format case.

## Built With

* [Node.js](https://nodejs.org/docs/v8.6.0/api/)
* [Mocha](https://mochajs.org/) - Test framework


## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/AhmedShab/Toy_Robot_Simulator/blob/master/LICENSE/) file for details
