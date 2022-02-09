# Application-of-Wavelet-Scattering-Network

This repo containes the different types of application of wavelet scattering transform.
It includes -
1. Signal denoising
2. Image denoising
3. Feature extraction
4. Image and Signal decomposition

<b> Extracting Features/Patterns in a price data using Wavelet Transform </b>
* Why Not use FFT or Fourier Transform to extract patterns or components in stock price data instead of using Wavelet transform directly?
Fourier Transform will work very well when the frequency spectrum is stationary. That is, the frequencies present in the signal are not time-dependent; if a signal contains a frequency of x Hz this frequency should be present equally anywhere in the signal.
The more non-stationary/dynamic a signal is, the worse the results will be.
Our Stock Data is dynamic in nature so the better approach to analyze dynamic signals is to use the Wavelet Transform instead of the Fourier Transform.

<b> Difference between Fourier Transform and Wavelet Transform </b>
1. Wavelet transform also transform the signal into its frequency domain, just like Fourie Transform The Difference is Fourier Transform has a very high resolution in the frequency domain and zero resolution in the time domain
2. Fourier transform(FT) is suitable for stationary signal where as Wavelet transform(WT) is suitable for both stationary and non-stationary signal.
3. FT convert signal from time domain to frequency domain signal, it provide two dimensional information i.e frequency componenet and applitude of the signal. WT gives complete three dimensional information about any signal. i.e difference frequency component present in a signal and their respective amplitudes and at time axis where these different frequency component exist.
4. FT has zero time resolution and very high frequency resolution. WT ha high time resolution and high frequeny resolution as well as time-frequecny resolution.
5. In FT signal is converted in to sine and cosine component. In WT signal is decompose into to mother and father wavelet.
6. FT is not suitable for study the local behaviour of the signal but WT is very suitable for study the local behaviour like discontinuity and spikes of the signal.
7. In FT the input can be real or complex function but the output is always complex In WT the input can be real or complex function and the output may be real or complex.
8. In layman's terms: A fourier transform (FT) will tell you what frequencies are present in your signal. A wavelet transform (WT) will tell you what frequencies are present and where (or at what scale). If you had a signal that was changing in time, the FT wouldn't tell you when (time) this has occurred. 

<b> So Using Fourier transform we get to know which frequencies are present in the signal but not at which time that frequency oscillates so How the scientist overcome this problem? </b>
<br>Short-Time Fourier Transform. In this approach, the original signal is split into several parts of equal length (which may or may not have an overlap) by using a sliding window before applying the Fourier Transform. The idea is quite simple: if we split our signal into 10 parts, and the Fourier Transform detects a specific frequency in the second part, then we know for sure that this frequency has occurred between 2/10 th and 3/10 th of our original signal.</br>
<br></br>
The main problem with this approach is that you run into the theoretical limits of the Fourier Transform known as the uncertainty principle. The smaller we make the size of the window the more we will know about where a frequency has occurred in the signal, but less about the frequency value itself. The larger we make the size of the window the more we will know about the frequency value and less about the time.
<br></br>
<b>The Wavelet Transform has:</b>
* for small frequency values a high resolution in the frequency domain, low resolution in the time- domain,
* for large frequency values a low resolution in the frequency domain, high resolution in the time domain.
<br></br>
<b>How does the Wavelet Transform work?</b>
<br>The Fourier Transform uses a series of sine-waves with different frequencies to analyze a signal. That is, a signal is represented through a linear combination of sine-waves.
The Wavelet Transform uses a series of functions called wavelets, each with a different scale. The word wavelet means a small wave, and this is exactly what a wavelet is.</br>
<br></br>
So a sine wave is from -inf to +inf while a wavelet exist for a particular duration which has a zero mean
There are many types of Wavelets.
