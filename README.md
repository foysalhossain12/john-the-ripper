# john-the-ripper part 1:




-------------------------  John The Ripper Part 1 : ---------------------------




Basic Command:

                        john target_file
                       
                       Example: 
                                       john hash.txt

                        john modes target_file
	
                        Example:
                                       john --single hash.txt

                                       john --wordlist hash.txt
                               
                                       john --incremental hash.txt

Best Command :
                        
                         john --format=hash_type --wordlist=wordlist target_file


                         Example:
 
                                       john --format=raw-md5 --wordlist=/usr/share/wordlist/rockyou.txt hash.txt


Hash:
        1.f9d4049dd6a4dc35d40e5265954b2a46 ------- 

       2.b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3 -----letmein

       3.1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032 ----

Note :
          Cracked Hash store in .pot path 
        
           /// john.pot ///

      
  # John the ripper part 2:
  
  

--------------John the ripper Part 2 ---------------

---------- SSH - RSA private key crack  --------

1.Convert  RSA private key into Hash using ssh2john.py 
  
    Command :

    /usr/share/john/ssh2john.py target_rsa_file > name.hash

2. Crack  name.hash value using john the ripper
      
    Command:

    john name.hash --wordlist=/usr/share/wordlist/rockyou.txt

3. Use this  password for  SSH Login  

Bonush:
            ssh -i  rsa_private_key username@ip

   
          ----    Zip File Password Crack --------

1. Convert the content of  target zip file into hash value 

  
                   zip2john zipfile.zip > zip_hash.txt



2. Crack password :
                              john --wordlist=/usr/share/wordlists/rockyou.txt zip_hash.txt

          
          ------- Rar File Password Crack --------

1.Convert into Hash:
                              rar2john rarfile.rar > rar_hash.txt

2.Crack password:
                        john --wordlist=/usr/share/wordlists/rockyou.txt rar_hash.txt



