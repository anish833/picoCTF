Challenge:
```
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with nc jupiter.challenges.picoctf.org 43522.
```

Connecting to the server will give a encrypted text
```
-------------------------------------------------------------------------------
ifaxqseh jcqc th uflq yosx - yqcblcaiu_th_i_frcq_oswnzs_fxywslaqsy
-------------------------------------------------------------------------------
mc mcqc afe wlij wfqc ejsa s blsqecq fy sa jflq fle fy flq hjtp etoo mc hsm jcq htak, saz ejca t lazcqheffz yfq ejc ytqhe etwc mjse msh wcsae nu s hjtp yflazcqtax ta ejc hcs.  t wlhe sikafmoczxc t jsz jsqzou cuch ef offk lp mjca ejc hcswca efoz wc hjc msh htaktax; yfq yqfw ejc wfwcae ejse ejcu qsejcq ple wc taef ejc nfse ejsa ejse t wtxje nc hstz ef xf ta, wu jcsqe msh, sh te mcqc, zcsz mtejta wc, psqeou mtej yqtxje, psqeou mtej jfqqfq fy wtaz, saz ejc ejflxjeh fy mjse msh uce ncyfqc wc.
```

It says it is a substitution cipher so I went to a website ```https://www.quipqiup.com/```. This website will deal with substition ciphers easily. After decoding I got the
text
```
congrats here is your flag - frequency_is_c_over_lambda_ogfmaunraf 
------------------------------------------------------------------------------- 
we were not much more than a quarter of an hour out of our ship till we saw her sink, and then i understood for the first time what was meant by a ship foundering in the sea. i must acknowledge i had hardly eyes to look up when the seamen told me she was sinking; for from the moment that they rather put me into the boat than that i might be said to go in, my heart was, as it were, dead within me, partly with fright, partly with horror of mind, and the thoughts of what was yet before me.
```

The flag is ```picoCTF{frequency_is_c_over_lambda_ogfmaunraf}```
