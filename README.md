# qosk_task1
This repository is created to share my solution task 1 with QOSF.

The task was: You have two integers, either positive or negative, and the challenge is to generate a quantum algorithm that returns which is the larger number. Consider an appropriate number of qubits and explain why your proposal is valid for all kinds of numbers in case. 

I implemented the algotithm using Qiskit, for which you'll find the code in the attached .ipynb file. The algorithm goes as follows:
1. Created two qubits and initialize them to the values of the input integers.
2. To compare the value of the qubits:
        . Applied a Hadamard gate to create a superposition.
        . Applied a CNOT gate where 1st qubit was controlled and the second qubit was target.
        . Applied another Hadamard to create a superposition. 
        . Measured the first qubit.
3. The only possible outcomes were |0> and |1>. If the outcome was |0⟩, it implied that the first integer was larger than the second integer. Otherwise, the second integer was larger than the first integer.
 
I had tested this algorithm for numbers of different digits and it worked fine for all of them.