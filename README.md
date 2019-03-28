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
    