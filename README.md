# Digital-wallet-circuit
> In one topic, you are going to design a simple digital wallet that is activated by getting a password and you can deposit money into it.
This circuit will be a sequential circuit.
For the security of the wallet, a 4-bit password is intended for it. By activating the pass_ch signal, you can enter the entry value. The amount of money saved will be 7 bits (from 0 to 127). 
This value is 0 by default and will be displayed at any moment through the out output.

How to work with the wallet: 
if the 4-bit password is entered correctly, the out_En output is set to one and one of the additional operations can be performed.
If the password is entered incorrectly, the out_En output is zero and no operation can be performed
The operation of adding money is to enter the desired amount of money in the 7-bit input
and set the sub/add signal to 0.
In this case, if the password is entered correctly, by pressing the button
apply, the input value is added to the previous value and stored in the wallet.

The operation of subtracting money is such that the amount
should be put on the desired money in the 7-bit input and set the sub/add signal to 1. In this case, if the password is correct
, by pressing the apply key, the input value is reduced from the previous value and stored in the wallet. by makin Reset signal equal to one the amount of money in the wallet should be zero

## scheme
![Screenshot (236)](https://user-images.githubusercontent.com/108394058/222352602-60d8de45-d5f6-41b6-8ee4-b7e52b375be1.png)
## U1 (4063)
> U1 is a comparator that compare the password of wallet with password that user gives to input
## U2 A (4013)
> is a d-ff that its output (EN_out) shows that the user is in wallet account or not
## B3 (BALANCE)
![Screenshot (237)](https://user-images.githubusercontent.com/108394058/222353114-b71815d9-7b21-4f7f-a7cc-07b9dd294cc4.png)
> B3 is balance and can save 7 bits (0-127)
## CP 1 (CHANGE PASS)
![Screenshot (232)](https://user-images.githubusercontent.com/108394058/222350771-caa5af03-8895-4b38-a3fb-eadb5f5cac98.png)
> CP 1 contains four d-ff to save 4 bits of password
## A/S (7 bit ADDER/SUBBER)
![Screenshot (238)](https://user-images.githubusercontent.com/108394058/222355157-8babd91c-6ac4-451d-9251-9becbc5ea692.png)
> it is used for adding or getting money fromm balance implemented by full adders ,mux and comparator
###### FULLADDER
![Screenshot (239)](https://user-images.githubusercontent.com/108394058/222356019-95c54df0-c44c-4263-972b-4a1e68e17c88.png)
> used to add bits (x and y are main bits and C_in is carry that has formed from previous plural)

###### MUX
![Screenshot (241)](https://user-images.githubusercontent.com/108394058/222357437-be22e928-b6bc-42fe-82da-3bf72ba95a38.png)
> uses S (bit that shows overflow or underflow) to avoid sum or sub becuase of overflow or underflow

###### COMP1 (7-BIT COMPARATOR)
![Screenshot (242)](https://user-images.githubusercontent.com/108394058/222359982-ceb27ecf-be00-49ba-ae5b-f566f1b04d13.png)
> comapre A(balance) and B(new input) and checks if B > A
