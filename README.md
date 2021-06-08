# Caesar_Cipher_decryption
package Caesar_Cipher;

import java.util.*;
public class Caesarcipher_decryption{
        public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println(" Enter the ciphertext message : ");
        String ciphertext = sc.nextLine();
        System.out.println(" Enter the shift value : ");
        int shift = sc.nextInt();
        String decryptMessage = "";
        for(int i=0; i < ciphertext.length();i++)  
        {
            char alphabet = ciphertext.charAt(i);
	            if(alphabet >= 'a' && alphabet <= 'z')
            {
                alphabet = (char) (alphabet - shift);
                if(alphabet < 'a') { 
                 alphabet = (char) (alphabet-'a'+'z'+1);
                }
                decryptMessage = decryptMessage + alphabet;
            }    
            else if(alphabet >= 'A' && alphabet <= 'Z')
            {
             alphabet = (char) (alphabet - shift);
                
               if (alphabet < 'A') {    

                }
                decryptMessage = decryptMessage + alphabet;            
            }
            else 
            {
             decryptMessage = decryptMessage + alphabet;            
            } 
        }
        System.out.println(" decrypt message : " + decryptMessage);
    }
}
