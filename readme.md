# Channel Estimation - Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]

Summary: Chirp involves signals whose phase evolves in some way over time, and can be found in many applications. For example, in Figures 1(a) and (B) [1]-[4], the spatial frequency of the near-field Fresnel diffraction pattern increases linearly with the distance from the screen's origin. In radar systems, linear frequency modulation signals sweep across a wide bandwidth spectrum at a constant amplitude. Pulse compression is achieved by correlating the echoes reflected from the target, much like transmitting and receiving "short" pulses. The position of the target can be resolved from time-delayed pulses [5]-[7]. In spread-spectrum systems, binary information is encoded by modulating the carrier frequency, scanning frequencies linearly from low to high as "up chirp" for bit "1", or from high to low as "down chirp" for bit "0", as shown in Figures 1(c) and (d) [8]-[13]. Linear frequency modulation pulse signals use a wideband spectrum, thus being resilient to harmful effects such as channel noise in wireless mobile channels, multipath fading, and Doppler effects.

For communication purposes, chirp waveforms are part of spread-spectrum technology, namely, linear frequency modulation (LFM) spread-spectrum (CSS), providing reliable and secure communication for military, underwater, and aerospace applications [14]-[16]. In the latest ultra-wideband (UWB) standard of the IEEE 802.15.4a group [17], CSS is adopted to meet the FCC requirements for the radiation power spectral mask of unauthorized UWB systems. At the same time, it achieves what UWB should do, ranging, measurement, and communication [18]-[20].
Traditionally, mature CMOS technology is typically utilized for generating chirp signals through surface acoustic wave (SAW) filtering methods or frequency modulation by piezoelectric oscillators [21]-[25]. In linear frequency modulation (LFM) or frequency modulation systems, a wide spectrum is occupied for modulating information. Due to the advantages of high processing gain and strong multipath interference resistance, linear frequency modulation sacrifices spectral efficiency. In a given period T and bandwidth B, only one modulated chirp exists, as shown in Figure 2(a). If multiple chirp signals exist within the same period and bandwidth, interference occurs. Therefore, linear frequency modulation is attractive for reliability-priority low data rate applications.
To enhance the data rate of UWB systems, multicode UWB proposes the division of the entire bandwidth into a set of spectrally separated chirps, as seen in Figure 2(a) [18]. It is modulated with binary codes (e.g., Walsh-Hadamard codes). The receiver retrieves information from the chirps across different subchannels throughout the bandwidth.
Inspirationally, in this paper, we consider the possibility of synthesizing a bank of chirps without any interference in the same period and bandwidth if their amplitudes and phases could be used for information modulation. Could we then adopt advanced digital signal processing techniques in the digital domain rather than the analog domain to achieve this system?
In this paper, we introduce the answer: Orthogonal Chirp Frequency Division Multiplexing (OCDM), which essentially represents the principle of orthogonally multiplexing multiple chirp waveforms across the same bandwidth towards maximum communication rate. As shown in Figure 2(B), in OCDM, a beam of chirp waveforms overlaps both temporally and spectrally. The phase and/or amplitude of the chirp can be modulated, for example, using Phase Shift Keying (PSK), Pulse Amplitude Modulation (PAM), or Quadrature Amplitude Modulation (QAM). We prove that the modulated chirps are orthogonal in chirp dimensionality, interfering mutually during transmission.
We have demonstrated that the fundamental principle of the OCDM system is the Fresnel transform, similar to the Fourier transform in OFDM. We proposed a digital implementation method for the OCDM system based on Discrete Fresnel Transform (DFnT). Specifically, the Inverse DFnT (IDFnT) generates the OCDM signal at the transmitter and the DFnT recovers the OCDM signal at the receiver.

Then, we analyzed the linear time-invariant (LTI) or quasi-static channels under which the OCDM signals are transmitted, which can be generalized to most practical communication channels, such as coaxial cables, optical fibers, and mobile radio channels, based on the convolutional characteristics of the Fresnel transform. It indicates that channel distortion can be compensated through use of either the time domain or frequency domain equalizers.

On this basis, we further proposed an OCDM channel equalization algorithm based on a single tap frequency domain equalizer (FDE), which has higher equalization efficiency than the above two equalization algorithms. Simulation results show that the performance of OCDM outperforms traditional OFDM, and it exhibits better tolerance to interference caused by insufficient guard interval (GI) length compared to a single carrier (SC) FDE system.

The organization of this paper is as follows: In Section 2, to support OCDM, we introduce the Fresnel transform and its discrete form DFnT. In Section 3, we introduce the proposed OCDM system. Section 4 studies the mathematical model of the OCDM system under an LTI channel. Additionally, we propose an effective equalization algorithm. Section 5 discusses the implementation of the OCDM system and its compatibility with OFDM systems. Section 6 evaluates the performance of the OCDM system under wireless multipath fading channels, and finally, we summarize this paper.
System Model
Simulation Results
Conclusion In this paper, we propose the OCDM system, which is fundamentally based on the principle of reusing a set of orthogonal chirp waveforms for high-speed communication. It achieves the maximum SE of the CSS system, just as OFDM does to FDM systems. The implementation of this system is based on Fresnel transform, and its convolution theorem provides an analytical method to simulate the transmission of OCDM signals over LTI channels. In OCDM, both time-domain and frequency-domain equalizers can be used for channel compensation. Through the characteristic decomposition of the DFnT matrix, a simple and effective single-tap equalizer algorithm is further proposed. Simulations under wireless multipath channels validate the effectiveness of the algorithm. The results show that OCDM outperforms traditional OFDM systems and also exhibits better interference resistance compared to DFT-P-OFDM and SC-FDE due to insufficient GI. Therefore, the proposed OCDM system can be an attractive alternative solution for high-speed communication systems.
MATLAB code verification

## Images

![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](01.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](02.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](03.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](04.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](05.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](06.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](07.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](08.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](09.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](10.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](11.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](12.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](13.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](14.jpg)
![(Channel Estimation)Orthogonal Linear Frequency-Modulated Diversity Multiplexing (OCDM) [with MATLAB Code + Paper]](15.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
