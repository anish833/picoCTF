Challenge:
```
This vault uses ASCII encoding for the password. The source code for this vault is here: VaultDoor4.java
```

They gave the java code
```
import java.util.*;

class VaultDoor4 {
    public static void main(String args[]) {
        VaultDoor4 vaultDoor = new VaultDoor4();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // I made myself dizzy converting all of these numbers into different bases,
    // so I just *know* that this vault will be impenetrable. This will make Dr.
    // Evil like me better than all of the other minions--especially Minion
    // #5620--I just know it!
    //
    //  .:::.   .:::.
    // :::::::.:::::::
    // :::::::::::::::
    // ':::::::::::::'
    //   ':::::::::'
    //     ':::::'
    //       ':'
    // -Minion #7781
    public boolean checkPassword(String password) {
        byte[] passBytes = password.getBytes();
        byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0143, 061 ,
            '9' , '4' , 'f' , '7' , '4' , '5' , '8' , 'e' ,
        };
        for (int i=0; i<32; i++) {
            if (passBytes[i] != myBytes[i]) {
                return false;
            }
        }
        return true;
    }
}
```

This code is simply encoded the flag and matching the input with the encoded flag. So we have to break the encoding. Check the ```myBytes``` bytearray which have the 
encoded flag the first line numbers ``` 106 , 85  , 53  , 116 , 95  , 52  , 95  , 98 ``` is ```Decimal encoded```, the second line numbers ``` 0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f``` are ```Hexademial```, the third line numbers are ``` 0142, 0131, 0164, 063 , 0163, 0137, 0143, 061``` are ```Octal Numbers``` and the
last line is ```'9' , '4' , 'f' , '7' , '4' , '5' , '8' , 'e'``` is not encoded. So decoding the values according to the encoding implemented and combining 
gave me the flag

flag:```picoCTF{jU5t_4_bUnCh_0f_bYt3s_c194f7458e}```







