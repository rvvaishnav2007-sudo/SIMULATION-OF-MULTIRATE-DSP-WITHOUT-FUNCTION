# EXP 6 : SIMULATION OF MULTIRATE DSP WITHOUT FUNCTION

## AIM: 

To perform and verify multirate DSP without function using SCILAB.

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM : 
      clear; 
      clc; 
      close; 
      n = 0:%pi/50:2*%pi; 
       
      x = sin(%pi*n); //original signal 
      M=input('Enter the downsampling factor'); 
      L=input('Enter the upsampling factor'); 
       
       
      //Down Sampling 
       
      downsampling_x = x(1:M:length(x)); 
      disp(x,'Input signal x(n)='); 
      disp(downsampling_x,'Downsampled Signal'); 
      figure(1); 
      subplot(2,1,1) 
      plot2d3(1:length(x),x); 
      xtitle('original singal') 
      subplot(2,1,2) 
      
      plot2d3(1:length(downsampling_x),downsampling_x); 
      xtitle('Downsampled Signal by a factor of M'); 
       
       
      //Upsampling 
      upsampling_x=[]; 
      for i=1:length(x) 
      upsampling_x(1,L*i)=x(i); 
      end 
      disp(x,'Input signal x(n)='); 
      disp(upsampling_x,'Upsampled Signal'); 
       
       
      figure(2); 
      subplot(2,1,1); 
      plot2d3(x); 
      title('original signal'); 
      subplot(2,1,2); 
      plot2d3(upsampling_x); 
      title('Upsampled Signal by a factor of L');

## OUTPUT: 
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/c832898e-bfd2-4d61-8939-11dc3ed802f1" />
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/566ff9ca-f803-4874-9f08-7075b9648f83" />


## RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented.
