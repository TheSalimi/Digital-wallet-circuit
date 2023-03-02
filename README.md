# Digital-wallet-circuit

## scheme
![Screenshot (236)](https://user-images.githubusercontent.com/108394058/222352602-60d8de45-d5f6-41b6-8ee4-b7e52b375be1.png)
## U1 (4063)
> U1 is a comparator that compare the password of wallet with password that user gives to input
## U2 A (4013)
> is a d-ff that its output (EN_out) shows that the user is in wallet account or not
## B3 (BALANCE)
![Screenshot (237)](https://user-images.githubusercontent.com/108394058/222353114-b71815d9-7b21-4f7f-a7cc-07b9dd294cc4.png)
> B3 is balance and can save 7 bits (0-255)
## CP 1 (CHANGE PASS)
![Screenshot (232)](https://user-images.githubusercontent.com/108394058/222350771-caa5af03-8895-4b38-a3fb-eadb5f5cac98.png)
> CP 1 contains four d-ff to save 4 bits of password
## A/S (7 bit ADDER/SUBBER)
![Screenshot (238)](https://user-images.githubusercontent.com/108394058/222355157-8babd91c-6ac4-451d-9251-9becbc5ea692.png)
> it is used for adding or getting money fromm balance implemented by full adders ,mux and comparator
###### FULLADDER
![Screenshot (239)](https://user-images.githubusercontent.com/108394058/222356019-95c54df0-c44c-4263-972b-4a1e68e17c88.png)
> used to add bits (x and y are main bits and C_in is carry that has formed from previous plural)
![Screenshot (239)](https://user-images.githubusercontent.com/108394058/222356524-bc1283c4-fe84-45f6-a3db-05e8c4a190b3.png)
