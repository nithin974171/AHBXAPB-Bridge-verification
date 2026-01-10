# AHBXAPB-Bridge-verification
The AHBtoAPB Bridge is an AHB slave, providing an interface between the high-speed AHB and the low-power APB. Read and write transfers on the AHB are converted into equivalent transfers on the APB. As the APB is not pipelined, then wait states are added during transfers to and from the APB when the AHB is required to wait for the APB. 
<img width="805" height="554" alt="image" src="https://github.com/user-attachments/assets/8e69e056-35ba-4dd2-801a-4a22f4401a01" />

The bridge unit converts system bus transfers into APB transfers and performs the following functions:

1) Latches the address and holds it valid throughout the transfer. 
2) Decodes the address and generates a peripheral select, PSELx. 
3) Only one select signal can be active during a transfer.
4) Drives the data onto the APB for a write transfer. 
5) Drives the APB data onto the system bus for a read transfer.
6) Generates a timing strobe, PENABLE, for the transfer.

8) <img width="648" height="485" alt="image" src="https://github.com/user-attachments/assets/5d67a9e3-3c94-4dba-8ed1-474ca977bfea" />
<img width="717" height="452" alt="image" src="https://github.com/user-attachments/assets/51984e5d-0ee8-4252-a9a9-e7da6cf39cad" />

Below ENV architecture 
<img width="1024" height="640" alt="image" src="https://github.com/user-attachments/assets/9350892e-83e8-4803-93aa-2a45bd88afdc" />


