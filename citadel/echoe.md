## Echoes and Pings  
You come across the remnants of a fallen corporation and the final network communication ever sent by  
them.   

Allegedly, the message contained an image that predicted the rise of the Citadel. Your task is to  
uncover what was sent and decode the communication to extract the passcode that will unlock the  
next floor.  
### Solve
**Flag** `citadel{1_r34lly_w4nt_t0_st4y_4t_y0ur_h0us3}`
I analyzed the pcap file's protocol hierachy, we see an image was sent.  
On analyzing the ICMP packets we see a jpg was sent on it. After spending a lot of time and admittedly a lot  
of chatgpt-ing we built a script to uncover the image.  
