# myAmazonbraket

https://docs.aws.amazon.com/braket/latest/developerguide/braket-get-started.html

https://docs.aws.amazon.com/braket/latest/APIReference/Welcome.html

https://aws.amazon.com/braket/faqs/

https://aws.amazon.com/blogs/quantum-computing/

https://quantumcomputing.stackexchange.com/



https://aws.amazon.com/quantum-solutions-lab/

https://aws.amazon.com/blogs/quantum-computing/announcing-the-opening-of-the-aws-center-for-quantum-computing/

https://aws.amazon.com/blogs/quantum-computing/announcing-the-aws-center-for-quantum-networking/


https://github.com/amazon-braket/amazon-braket-examples

https://github.com/amazon-braket/amazon-braket-algorithm-library


How is Amazon Braket used to architect a cloud solution?

Braket provides on-demand access to quantum computing devices, including on-demand circuit simulators and different types of QPUs. In Braket, the atomic request to a device is a quantum task. For gate-based QC devices, this request includes the quantum circuit (plus the measurement instructions and number of shots) and other request metadata. For Analog Hamiltonian Simulation (AHS), the task contains the physical layout of the quantum register and the time and space dependence of the manipulating fields.

To learn more, choose each of the five numbered markers in the following diagram.









**What are the basic technical concepts of Amazon Braket?**

To learn more about the basic technical concepts of Braket, expand each of the following nine categories.


Quantum circuit
–
A quantum circuit is the instruction set that defines a computation on a gate-based quantum computer. A quantum circuit is a sequence of quantum gates together with measurement instructions.



Quantum processing unit
–
A QPU is a physical quantum computing device where you can run a quantum task. Braket provides AWS customers with access to quantum computing technologies from multiple quantum hardware providers. This includes superconducting, trapped ion, and neutral-atom quantum computers. To learn more, see Amazon Braket Supported Devices(opens in a new tab) in the Amazon Braket Developer Guide.



Device
–
In Braket, a device is a QPU or simulator that you can call to run quantum tasks. Braket provides access to QPU devices from quantum hardware providers, on-demand simulators, local simulators, and embedded simulators. For all devices, you can find device properties, such as device topology, calibration data, and native gate sets, on the Devices page of the Amazon Braket console. You can also find device properties through the Braket API.


Task
–
In Braket, a task or quantum task is the atomic request to a device. For gate-based quantum computing devices, this includes the quantum circuit, including the measurement instructions and number of shots and other requested metadata. For AHS, the task contains the physical layout of the quantum register and the time dependence and space dependence of the manipulating fields.

You can create quantum tasks through the Braket SDK or by using the CreateQuantumTask API operation directly. After you create a task, it is queued until the requested device becomes available. You can view your quantum tasks on the Tasks page of the Amazon Braket console or by using the GetQuantumTask or SearchQuantumTasks API operations.


Shots
–
Because quantum computing is inherently probabilistic, any circuit needs to be evaluated multiple times to get an accurate result. A single circuit evaluation and measurement is called a shot. The number of shots, or repeated evaluations, for a circuit is based on how accurate you want the result to be. The number of shots can range from 10–100,000 shots per task.


Braket Notebook Instances
–


A Braket Notebook Instance is a Jupyter notebook instance fully managed by Amazon Braket. The Amazon Braket notebook instances are based on Amazon SageMaker notebook instances and come pre-installed with the Amazon Braket SDK, example tutorials, and plugins. You can launch Braket Notebook Instances from the AWS Management Console.



Braket local simulators
–


The local simulators are included in the Amazon Braket SDK at no cost. They can run on your laptop or within an Amazon Braket managed notebook. You can use them for quick validation of circuit designs. They are well suited for small and medium-scale simulations – up to 25 qubits without noise, or up to 12 qubits with noise, depending on your hardware.



Braket on-demand simulators
–


Braket includes access to fully managed on-demand simulators. All on-demand simulators automatically scale AWS computing resources to deliver high-performance execution of your quantum algorithms. The cost of using the Amazon Braket on-demand simulators is based on the duration of each simulation task. When you use on-demand simulators, you are billed at a per-minute rate, in increments of one millisecond, for the time your simulation takes to run, with a minimum billing duration of 3 seconds per simulation.

Amazon Braket Hybrid Jobs
–
Amazon Braket Hybrid Jobs provides additional support for hybrid quantum-classical algorithms. You can run fully managed hybrid algorithms that combine AWS classical compute resources based on Amazon EC2, or the job instance, with Braket QPUs or quantum circuit simulators. While your job is running, it has priority access to the selected target QPU, AND tasks from your job run ahead of other tasks queued on the device. This results in shorter, more predictable runtimes for hybrid algorithms.



For hybrid variational algorithms, the QPUs act as coprocessors to classical computers. This is similar to how a graphics processing unit (GPU) is used in training machine learning models. Such hybrid algorithms rely on iterative computations between classical computers and QPUs or simulators.



With the Braket Hybrid Jobs feature, Braket coordinates the necessary quantum and classical compute resources. It then runs your algorithm and releases the resources after the job is complete, so you pay only for what you use.



For more information on Hybrid Jobs, visit Introducing Amazon Braket Hybrid Jobs – Set Up, Monitor, and Efficiently Run Hybrid Quantum-Classical Workloads(opens in a new tab) in the AWS News Blog.


S3 bucket
–
Amazon S3 is an AWS service you can use to store data as objects in buckets. The total volume of data and number of objects you can store in Amazon S3 are unlimited. Individual Amazon S3 objects can range in size from a minimum of 0 bytes to a maximum of 5 TB.  You can upload any type of file data to an S3 bucket. Examples include images, videos, text files, backup files, media files for a website, archived documents, and your Braket task results.



IAM roles
–
An AWS Identity and Access Management (IAM) role is an identity that you can assume to gain access to permissions. Before a user, application, or service can assume an IAM role, they must be granted permissions to switch to the role. When someone assumes an IAM role, they abandon all previous permissions they had under a previous role and assume the permissions of the new role.



Best practice: IAM roles are ideal when access to services or resources needs to be granted temporarily instead of long-term.


IAM policies
–
An IAM policy is a document that grants or denies permissions to AWS services and resources. With IAM policies, you can customize a user’s level of access to resources. For example, you can grant users access to all S3 buckets in your AWS account or only a specific bucket.

 

Best practice: Follow the security principle of least privilege when granting permissions. By following this principle, you help prevent users or roles from having more permissions than needed to perform their tasks. For example, if an employee needs access to only one bucket, specify the bucket in the IAM policy. You do not need to grant the employee access to all the buckets in your AWS account.



**What programming languages can you use with Amazon Braket?**

To learn more about using programming languages with Braket, expand each of the following five sections.


Python SDK
+

PennyLane
+

Qiskit
+

Julia
+

Open Quantum Assembly Language


https://github.com/amazon-braket/amazon-braket-sdk-python

https://pypi.org/project/amazon-braket-sdk/

https://docs.pennylane.ai/en/stable/

https://aws.amazon.com/blogs/quantum-computing/introducing-the-qiskit-provider-for-amazon-braket/

https://github.com/amazon-braket/Braket.jl

https://docs.aws.amazon.com/braket/latest/developerguide/braket-references.html


**What is quantum computing?**

Essentially, quantum computing is a new way of processing information that uses quantum coherence and entanglement. It has the potential to solve computational problems beyond the reach of classical computers by using the laws of quantum mechanics.

Quantum computers solve problems fundamentally differently than conventional information processing. Instead of using traditional CPU and memory models, qubits—the building blocks of a quantum computer—are used to store and process quantum information.

While quantum computers have the potential to be disruptive, we are still in the early stages of this technology. Significant scientific and engineering challenges need to be overcome before customers can use quantum computing to address business problems.


A new paradigm for computation that uses the laws of quantum physics


A way to solve problems in novel ways and access a new class of problems


How to build these sensitive devices is a difficult scientific challenge



Wide interest in possible quantum solutions

You might wonder why a quantum computer can provide speedups for some problems but not for others. A quantum computer has a different model of computation than conventional computers. In this model, there are algorithms that, for certain problems, are exponentially faster than the fastest possible—or fastest known—classical algorithms.

For example, there is no known classical algorithm to perform integer factoring in a reasonable amount of time. This task is known to be efficiently solvable using quantum resources.

Discovering new algorithms where quantum computers are more efficient than their classical counterparts is an active area of research. The original promise of quantum computers came from the famous physicist, Richard Feynman. He postulated that a quantum computer is the best tool for studying certain classes of problems, namely simulating the physics of quantum systems.

**What are the basic technical concepts of Braket?**

Users of Braket should have a basic understanding of the following concepts. To learn more, expand each of the following four categories.




QPU
A QPU is a physical quantum computing device where you can run a quantum task. Braket provides AWS customers with access to quantum computing technologies from multiple quantum hardware providers. This includes superconducting, trapped ion, and neutral-atom quantum computers. For the most up-to-date information about supported QPUs, see Amazon Braket Supported Devices(opens in a new tab).


Device
In Braket, a device is a QPU or simulator that you can call to run quantum tasks. Braket provides access to QPU devices from quantum hardware providers, on-demand simulators, local simulators, and embedded simulators. For all devices, you can find further device properties, such as device topology, calibration data, and built-in device gate sets, on the Devices tab of the Braket console or by using the Braket API and Braket SDK.


Quantum task
In Braket, a quantum task is the atomic request to a device. For gate-based quantum computing devices, this request includes the quantum circuit plus the measurement instructions, number of shots, and other request metadata. For Analog Hamiltonian Simulation (AHS), the task contains the physical layout of the quantum register and the time dependence and space dependence of the pulse schedule.

You can create quantum tasks through the Amazon Braket SDK or by using the Braket API operation directly. After you create a task, it is queued until the requested device becomes available. You can view your quantum tasks on the Tasks page of the Braket console or by using the GetQuantumTask or SearchQuantumTasks API operations. For more information, see Amazon Braket Terms and Concepts(opens in a new tab) in the Developer Guide and the Amazon Braket API Reference(opens in a new tab).


Shots
Because quantum computing is inherently probabilistic, any circuit needs to be evaluated multiple times to get an accurate result. A single circuit evaluation and measurement is called a shot. The number of shots, or repeated evaluations, for a circuit is based on how accurate you want the result to be.

**How to use Braket**

Braket structures the experience for scientists and developers to explore quantum computing from the ideation stage to running algorithms on quantum devices. Braket provides tools to help you build tasks.

Tasks are standalone requests of a device. Such requests include a quantum circuit or an Analog Hamiltonian Simulation program along with the number of shots to be performed. Braket provides tools to help you build the tasks, test them on simulators, and run them on QPUs.

Many quantum algorithms require interacting over numerous tasks to learn the outcome of the algorithm. Amazon Braket Hybrid Jobs helps run hybrid quantum-classical workloads faster, more efficiently, and more predictably.

https://docs.aws.amazon.com/braket/latest/developerguide/security.html



**How is Braket used to architect a cloud solution?**

Braket provides on-demand access to quantum computing devices, including on-demand circuit simulators and different types of QPUs. In Braket, the atomic request to a device is a quantum task (the equivalent of a job in the Qiskit framework). 

For gate-based quantum computing devices, this request includes the quantum circuit plus the measurement instructions, number of shots, and other request metadata. For Analog Hamiltonian Simulation, the task contains the physical layout of the quantum register and the time and space dependence of the manipulating fields. A third paradigm for defining tasks uses Braket Pulse to issue analog instructions that control the qubits of the QPU.

To learn more, choose each of the five numbered markers in the following diagram.

Architecture diagram of task flow within Amazon Braket.

![image](https://github.com/user-attachments/assets/72c4f44b-83b4-4fde-800d-d8c56dc0690e)


**A Python example** of how to run a two-qubit circuit is as follows. In the code snippet following this diagram, the SDK polls for the results in the background and loads them into the Jupyter notebook, Amazon Braket Hybrid Jobs, or the local environment at task completion.


View code example
# choose the on-demand simulator to run the circuit

from braket.aws import AwsDevice

# or choose the local simulator

from braket.devices import LocalSimulator

from braket.circuits import Circuit, Observable

#device = device = AwsDevice(Devices.Amazon.SV1)

device = LocalSimulator()

# create a circuit with a result type

circ = Circuit().rx(target=0, angle=1).ry(target=1, angle=0.2).cnot(0,2)

# add another result type

circ.probability(target=[0, 2])

# submit the task to run

my_task = device.run(circ, shots=1000)

# get results of the task

result = my_task.result()

print(result.measurement_counts)

**Using examples from the Braket tutorials repository**

The Braket Tutorials GitHub is the primary repository for Braket tutorials. To help you get started, there are tutorials on quantum computing using Braket. There are tutorials for getting started, Braket features, and use cases. For more information, including examples of how to use Braket, see Braket Tutorials(opens in a new tab) on GitHub.

Creating tasks using Qiskit and the Qiskit-Braket provider

You can run algorithms written with a few lines of code in Qiskit, a widely used open source quantum programming SDK. You can run Qiskit code directly on Braket with the Qiskit-Braket provider. 



**Curated resources**

For additional resources on topics related to this lesson, expand each of the following three categories.


Building circuits, tasks, and hybrid jobs
For more information about building circuits, tasks, and hybrid jobs on Braket, see the following resources:

Anatomy of Quantum Circuits and Quantum Tasks in Amazon Braket(opens in a new tab)
https://github.com/aws/amazon-braket-examples/blob/main/examples/getting_started/3_Deep_dive_into_the_anatomy_of_quantum_circuits/3_Deep_dive_into_the_anatomy_of_quantum_circuits.ipynb

Getting Started with OpenQASM on Braket(opens in a new tab)
https://github.com/aws/amazon-braket-examples/blob/main/examples/braket_features/Getting_Started_with_OpenQASM_on_Braket.ipynb

Amazon Braket Examples: Braket Features(opens in a new tab)
https://github.com/aws/amazon-braket-examples/tree/main/examples/braket_features

AWS Open-Sources OQpy to Make It Easier to Write Quantum Programs in OpenQASM 3(opens in a new tab)
https://aws.amazon.com/blogs/quantum-computing/aws-open-sources-oqpy-to-make-it-easier-to-write-quantum-programs-in-openqasm-3/

Building with PennyLane
For more information about using PennyLane with Braket, see the following resources:

Combining PennyLane with Amazon Braket(opens in a new tab)
https://github.com/aws/amazon-braket-examples/blob/main/examples/pennylane/0_Getting_started/0_Getting_started.ipynb

Creating a Bridge between Machine Learning and Quantum Computing with PennyLane(opens in a new tab)
https://aws.amazon.com/blogs/opensource/creating-a-bridge-between-machine-learning-and-quantum-computing-with-pennylane/

Building with Qiskit
For more information about using Qiskit with Braket, see the following resources:

How to Run Qiskit on Amazon Braket(opens in a new tab)(opens in a new tab)
https://github.com/aws/amazon-braket-examples/blob/main/examples/qiskit/0_Getting_Started.ipynb

Introducing the Qiskit Provider for Amazon Braket
https://aws.amazon.com/blogs/quantum-computing/introducing-the-qiskit-provider-for-amazon-braket/

