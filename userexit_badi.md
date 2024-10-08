### How to find a User Exit or BADI from debugger.

When we are trying to find a User Exit or a BADI, we can use some features of the debugger.

On top menu, we click:
Breakpoints -> Breakpoint at -> Breakpoint at Statement

![image](https://github.com/user-attachments/assets/1e3f41ff-c4c3-44cd-86e1-5b25401b576c)

On the below popup, on ABAP Cmnds 

![image](https://github.com/user-attachments/assets/e9767ae2-74a7-41a7-8fe8-8c97cb3e9e33)

We can put breakpoints on the followings statements:
- User exits: CALL CUSTOMER-FUNCTION
- BADI: CALL BADI

Also, for the BADI we can insert on the second tab 

![image](https://github.com/user-attachments/assets/c2863f2c-3f41-4aa8-a320-b81ff5acbee8)

the following class that is triggered before the call of the BADI’s.

- Class name: CL_EXITHANDLER
- Method Name: GET_INSTANCE

<div class="note">
   <strong>NOTE:</strong> The use of CL_EXITHANDLER-GET_INSTANCE is for Classic BADI.
  <br>The use of CALL BADI is for Kernal BADI.
    <br><br> Classic BADI:
  <br><ul><li>Interface name automatically generated</li>
  <br><li>Implementing class name automatically created</li>
  <br><li>Uses proxy class (CL_EXITHANDLER)</li>
  <br><li>Not using Fallback Class</li>
  <br><li>Implementation done in SE19</li></ul>
  <br> Kernal BADI:
  <br><ul><li>We have to create interface</li>
  <br><li>Implementing class name, we need to give</li>
  <br><li>Not uses proxy class</li>
  <br><li>Execution time less</li>
  <br><li>Uses Fallback Class</li></ul>
  </div>

