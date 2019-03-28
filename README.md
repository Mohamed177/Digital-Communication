# Digital Communication Project

A Simulation of the performance of different modulation schemes, BPSK, QPSK, FSK, QAM(16-64) in an AWGN environment.

- __General instructions to reproduce the figures:__
	 - Open Matlab then click on simulink's icon in the menu or simply write "simulink" in the matlab's Command Window.
	 - Open a Blank Model
	 - Add the needed blocks: (to edit the parameters of a certain block, just double-click it)
	 	- Random Integer Generator (Source of intital seed: parameter, Samples per frame: 100).
	 	- The modulator and demodulator.
	 	- AWGN channel (Eb/No (db): 10).
	 	- 2 Constellation Diagrams for before and after noise scatter diagram.
	 	- Error Rate Calculation block.
	 	- Display block.
	 - to Draw the BER diagrams:
	 	- Add ToWorkspace block (simout) (Variable name: ber, Save format: array, Save 2-D signals as: 2-D array) 
	 	- After saving the Model type "bertool" in the matlab's Command Window.
	 	- In the theoretical tab set (Eb/No range: -10:10, modulation type) and click plot
	 	- In Monte Carlo tab set (Eb/No range: -10:1:10), browse the saved simulink model, set the BER variable name to "ber" and click run
	 	
## BPSK

The simplest and most straightforward type of PSK is called binary phase shift keying (BPSK), where “binary” refers to the use of two phase offsets (one for logic high, one for logic low), It uses two phases which are separated by 180° and so can also be termed 2-PSK.

- __Extra instructions to reproduce the figures:__
	- Random Integer Generator(Set size: 2)

### - Figures:

* #### Scatter Diagrams Before Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/BPSK/BPSK_befNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/BPSK/BPSKrc_befNoise.JPG) 
    
* #### Scatter Diagrams After Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/BPSK/BPSK_aftNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/BPSK/BPSKrc_aftNoise.JPG) 
    
* #### BER performance figure
	
    ![BERvsSNR](/BPSK/BPSKrc_BERvsSNR.JPG)

	
## QPSK

QPSK is a modulation scheme that allows one symbol to transfer two bits of data. There are four possible two-bit numbers (00, 01, 10, 11), and consequently we need four phase offsets. Again, we want maximum separation between the phase options, which in this case is 90°.

- __Extra instructions to reproduce the figures:__
	- Random Integer Generator(Set size: 4)

### - Figures:

* #### Scatter Diagrams Before Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QPSK/QPSK_befNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QPSK/QPSKrc_befNoise.JPG) 
    
* #### Scatter Diagrams After Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QPSK/QPSK_aftNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QPSK/QPSKrc_aftNoise.JPG) 
    
* #### BER performance figure
	
    ![BERvsSNR](/QPSK/QPSK_BERvsSNR.JPG)
	
## FSK

Frequency-shift keying (FSK) is a frequency modulation scheme in which digital information is transmitted through discrete frequency changes of a carrier signal.

- __Extra instructions to reproduce the figures:__
	- Random Integer Generator(Set size: 2)

### - Figures:

* #### Scatter Diagrams Before Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/FSK/FSK_befNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/FSK/FSKrc_befNoise.JPG) 
    
* #### Scatter Diagrams After Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/FSK/FSK_aftNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/FSK/FSKrc_aftNoise.JPG) 
    
* #### BER performance figure
	
    ![BERvsSNR](/FSK/FSK_BERvsSNR.JPG)

	
## QAM 16

Quadrature amplitude modulation (QAM) is the name of a family of digital modulation methods and a related family of analog modulation methods widely used in modern telecommunications to transmit information. It conveys two analog message signals, or two digital bit streams, by changing (modulating) the amplitudes of two carrier waves, using the amplitude-shift keying (ASK) digital modulation scheme or amplitude modulation (AM) analog modulation scheme.

- __Extra instructions to reproduce the figures:__
	- Random Integer Generator(Set size: 16)

### - Figures:

* #### Scatter Diagrams Before Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QAM16/QAM16_befNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QAM16/QAM16rc_befNoise.jpg) 
    
* #### Scatter Diagrams After Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QAM16/QAM16_aftNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QAM16/QAM16rc_aftNoise.jpg) 
    
* #### BER performance figure
	
    ![BERvsSNR](/QAM16/QAM16_BERvsSNR.jpg)
	
## QAM 64

- __Extra instructions to reproduce the figures:__
	- Random Integer Generator(Set size: 64)

### - Figures:

* #### Scatter Diagrams Before Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QAM64/QAM64_befNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QAM64/QAM64rc_befNoise.jpg) 
    
* #### Scatter Diagrams After Noise
	
    Without Raised Cosine Filter:
    
	![without RCF](/QAM64/QAM64_aftNoise.jpg) 
    
    With Raised Cosine Filter:
    
    ![with RCF](/QAM64/QAM64rc_aftNoise.jpg) 
    
* #### BER performance figure
	
    ![BERvsSNR](/QAM64/QAM64_BERvsSNR.jpg)