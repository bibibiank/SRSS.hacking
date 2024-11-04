## Objetivo 

Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: [VaultDoorTraining.java](https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java)

## Solución  


```java

──(kali㉿kali)-[~/Downloads]
└─$ cd vaultDoorTraining 
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/vaultDoorTraining]
└─$ wget https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java
--2024-11-04 11:33:40--  https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 943 [application/octet-stream]
Saving to: ‘VaultDoorTraining.java’

VaultDoorTraining.java       100%[=============================================>]     943  --.-KB/s    in 0s      

2024-11-04 11:33:49 (23.3 MB/s) - ‘VaultDoorTraining.java’ saved [943/943]

                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/vaultDoorTraining]
└─$ ls                                                            
VaultDoorTraining.java
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/vaultDoorTraining]
└─$ cat VaultDoorTraining.java                                    
import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
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

    // The password is below. Is it safe to put the password in the source code?
    // What if somebody stole our source code? Then they would know what our
    // password is. Hmm... I will think of some ways to improve the security
    // on the other doors.
    //
    // -Minion #9567
    public boolean checkPassword(String password) {
        return password.equals("w4rm1ng_Up_w1tH_jAv4_be8d9806f18");
    }
}
                                                                                                                  

```
## Notas Adicionales 

### Referencias



