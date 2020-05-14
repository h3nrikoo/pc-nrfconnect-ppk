# nRF Connect Power Profiler with hacky data export feature
This fork exists because the otherwise brilliant nRF Connect Power Profiler does not support data exporting (yet?). 
This project is entirely based on [this equally hacky solution](https://github.com/fellerts/pc-nrfconnect-ppk), 
but had an outdated fork so I simply redid the changes on a new fork. I also modified it a bit for usage of windows. 
(only where to save the file). 

- When you stop measurements, the entire average buffer is written to Users\"user name"\AppData\Local\Temp\x_average.ppkdata
- The first value is the sample rate to create a t-axis in your plot, followed by an array containing all the sample values: 
 sampleRate\[val0, val1, ..., valn]
- It is badly formatted, but it works.

##How to use it 

0. Install nRF connect 

1. Clone repo into: 
    - Linux/macOS: `cd $HOME/.nrfconnect-apps/local`
    - Windows: `cd %USERPROFILE%/.nrfconnect-apps/local`

2. Download and install Node.js

3. Build the thing 
    - go to repo folder 
    - run `npm install` in your terminal to install dependencies 
    - run `npm run dev' in your terminal to build the app 

5. If you receive errors, learn Node.js (I have not)

6. Open nrF connect -> Power Profiler (exportable data)

7. After stopping a measurement the console should print "Wrote buffer (N samples to %USER%\AppData\Local\Temp\x_average.ppkdata" 
    -If it does not, an error was thrown, see step 5

# nRF Connect Power Profiler

Power Profiler app for [nRF Connect](https://github.com/NordicSemiconductor/pc-nrfconnect-launcher).

## Introduction

*nRF Connect Power Profiler* is a tool to communicate with the The Power Profiler Kit (PPK), an affordable and flexible tool to obtain real-time current measurements of your designs.
The PPK measures current consumption for a connected nRF5x Development Kit or any external board. It measures current from 1 μA up to 70 mA and gives a detailed picture of the current profile for the user application.

All functionality is described in the [User Guide](https://infocenter.nordicsemi.com/topic/ug_ppk/UG/ppk/PPK_user_guide_Intro.html).

![screenshot](resources/screenshot.gif)

## Installation

See the [InfoCenter](https://infocenter.nordicsemi.com/index.jsp?topic=%2Fstruct_nrftools%2Fstruct%2Fnrftools_nrfconnect.html) pages for information on how to install the application.

## Development

See the [app development](https://nordicsemiconductor.github.io/pc-nrfconnect-docs/) pages for details on how to develop apps for the nRF Connect for Desktop framework.

## Feedback

Please report issues on the [DevZone](https://devzone.nordicsemi.com) portal.

## Contributing

See the [infos on contributing](https://nordicsemiconductor.github.io/pc-nrfconnect-docs/contributing) for details.

## License

See the [LICENSE](LICENSE) file for details.
