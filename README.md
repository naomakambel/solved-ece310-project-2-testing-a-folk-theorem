Download Link: https://assignmentchef.com/product/solved-ece310-project-2-testing-a-_folk-theorem
<br>
One area in which discrete-time signal processing has enjoyed widespread use is in the field of speech processing. In this project we consider various issues relating to applying digital filtering to speech. Specifically, in this project, we consider the effect of all-pass filtering on speech.

Historically, DSP courses have put considerable emphasis on design techniques for both IIR and FIR filters, as discussed in Chapter 7 of the course text. A variety of filter design algorithms are now implemented in common software packages such as fdatool in Matlab. This makes it unnecessary for most practitioners to learn the details of the design algorithms; however, ceding the design function to a software package makes it more important to understand the properties of different types of optimal filters, the meanings of the design parameters, and some of the trade-offs between filter classes.

In the context of IIR filter design, we suggest that you read Sections 7.0 and 7.1 including Example 7.1.

Project Assignment

Your writeup should have a summary of how you went about this project (anywhere from one to five pages, not to exceed five pages). In addition to the five page maximum, you can include any appropriate Matlab plots. Do NOT turn in any Matlab code. The total number of pages including description and plots should not exceed ten pages.

The writeup will receive a grade which reflects our assessment of your level of understanding of the various issues involved and the effort that you put into it.

<h1>Playing Sound in Matlab</h1>

Throughout this project it will be necessary to play audio files which you will have manipulated in Matlab. The functions sound and soundsc (sound scaled) work well for doing this on most hardware platforms.

<h1>Introduction</h1>

A common “folk theorem” states that the ear is insensitive to phase, i.e. that for audio, phase distortion is inaudible. If that is correct, then processing audio with an all-pass filter should not result in perceived distortion. This project tests this conjecture. The all-pass filter that we consider is of the form

.

For this part of the project, the file projIA.mat will need to be first loaded into Matlab. To access the project zip file, click on the link below where you found this file on the web site. After downloading the zip file, copy its contents into your Matlab working directory and type load projIA. The b<sub>k</sub> and a<sub>k</sub> coefficients above are stored in the variables b and a respectively; b(k + 1)= b<sub>k</sub> and a(k + 1)= a<sub>k</sub>.

<ul>

 <li>Implement the all-pass filter for N = 1 and show plots of the impulse response (the first 100 samples), the magnitude of the frequency response, and the group delay.</li>

 <li>Plot the pole-zero diagram. You may find the functions roots and zplane helpful in doing so.</li>

 <li>Process the speech file, stored as the variable speech (sampled at rate f<sub>s</sub> = 11025 Hz), using the command filter to run the filter implemented in (a). Listen to the result and comment specifically on whether there is audible distortion.</li>

 <li>Implement the filter for N = 50 and again show plots of the impulse response (the first 5000 samples), the magnitude of the frequency response, and the group delay. Note: This is the hard part of the exercise, you can’t skip it.</li>

 <li>Repeat (c) with N = 50. How would you subjectively describe the distortion and what aspect of the filter is its primary cause?</li>

</ul>