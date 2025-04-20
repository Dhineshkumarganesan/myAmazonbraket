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


