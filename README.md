# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM
### D Flip Flop

![Screenshot 2023-11-22 141225](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/fa9165f1-2bb4-43a4-8ec0-491b40417a7c)


### JK Flip Flop

![Screenshot 2023-11-22 144129](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/a1cd8196-b124-4fa5-8e05-144ae074021c)


### SR Flip Flop

![Screenshot 2023-11-26 150316](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/81d4d225-8550-4396-8921-694a615dae47)


### T Flip Flop

![Screenshot 2023-11-26 152303](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/8353c24d-f711-4663-a0d2-78386399e18c)


/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Pradeep kumar 
RegisterNumber:  23006358
*/


###TRUTH TABLE

### D Flip Flop

![WhatsApp Image 2023-11-30 at 11 42 28 PM (1)](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/04a6233c-be45-4f0e-9cfc-e951eff6b65f)


### JK Flip Flop

![WhatsApp Image 2023-11-30 at 11 42 28 PM](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/85c2044d-ba8a-4185-9139-913920ae5fbc)


### SR Flip Flop

![srf truth table](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/33431b36-a896-439b-aa2a-f19fc1b63917)



### T Flip Flop

![WhatsApp Image 2023-11-30 at 11 42 28 PM (2)](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/4d59ab3d-192e-494f-b326-b387a0d911e1)





### RTL LOGIC FOR FLIPFLOPS 

### D Flip Flop

![Screenshot 2023-11-22 140109](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/19681696-c16d-4d7f-b2ce-f1502ca5803f)


### JK Flip Flop

![Screenshot 2023-11-22 144103](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/516f0dcf-67d8-48ba-95cb-e1faf83bfb00)


### SR Flip Flop

![Screenshot 2023-11-26 150301](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/456af602-4c15-4aba-a97f-73903ed8ae5d)


### T Flip Flop

![Screenshot 2023-11-26 152245](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/d313a699-9735-442b-a7a1-0ce2091d9b1f)







### TIMING DIGRAMS FOR FLIP FLOPS 

### D Flip Flop

![Screenshot 2023-11-22 140018](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/2bea8c76-c548-4b93-91dc-32f97c8568de)

### JK Flip Flop

![Screenshot 2023-11-22 144002](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/94234daf-cecc-4baa-960b-8395f85341a9)

### SR Flip Flop

![Screenshot 2023-11-26 150231](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/03bbc56d-3e4b-41b8-982f-d51afcb7e448)

### T Flip Flop

![Screenshot 2023-11-26 152213](https://github.com/Pradeepkumar-2005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147474038/1e9a9ae5-0612-4040-a220-2f89308e80fc)







### RESULTS 
