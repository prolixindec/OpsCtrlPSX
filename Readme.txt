0. RELEASE NOTES

This is a public beta release of this app, and there may still be some unpredictable behavior and glitches. We shall see. Please use at your own risk.

Since the last main update:
 
- Supported SimBrief flight plan format is now LIDO
- It is no longer necessary to download a .route file from SimBrief. OpsCtrlPSX constructs the .route file from the OFP.


1. OVERVIEW

This app does two main tasks: First, it parses a LIDO operational flight plan (OFP) that you drag-and-drop into the app, and it loads flight plan data (winds aloft, ZFW, etc.) into PSX. Second, it simulates interacting with a fictional Operations Control desk (OpsCtrl) provided by your company, so that you can obtain a final loadsheet after the aircraft doors have been closed.

When pilots receive an OFP, it has been generated with expected numbers as regards passenger load and freight. But in reality, some passengers don't show up, or more standby passengers can be accommodated. Or one pallet of freight doesn't make it in time, or there is an unexpected volume of mail to carry. Therefore, the final loadsheet is usually somewhat different than what the OFP predicted.

This app takes the OFP into consideration and applies random values so that your final weight and CG have some realistic variations compared to the flight planned values.


2. INSTALLATION

Install OpsCtrlPSX in any folder.


3. CONFIGURATION

On the Network tab in the app, set the IP address and port of your PSX server instance. You can also specify the MCDU line on which the OpsCtrl app appears (on the center MCDU). Make sure that the line you choose for OpsCtrl doesn't conflict with any other modules you are running. These preferences are saved in an .INI file located in /AppData/Roaming/OpsCtrlPSX


4. PREFLIGHT

Create an OFP with SimBrief using the LIDO format. Drag-and-drop the a PDF version of your OFP into the app. Click on "Load All into PSX" to copy the wind corridor, the flight-planned ZFW, the fuel (using the PSX fuel upload animation), and the route name into PSX. Alternatively, you can do these steps one by one, if needed.

Note 1: OpsCtrl builds a .route file for PSX from your OFP. You do not need to download a .route file from SimBrief. All you need is the OFP.

Note 2: OpsCtrl doesn't load the route into the FMC. It just sets your OFP's route as the one that will be loaded when you REQUEST the route from the FMC's RTE page.


5. FINAL LOADSHEET

When loading is completed, go to the center MCDU and select OPSCTRL. Now you will see a blank form, into which you can request final load data. After requesting the data, you will see the flight-planned ZWF plus a random addition or subtraction. The "TAKEOFF ZFW" and "TAKEOFF CG" have been entered into the PSX aircraft, so you should update the FMC with these values. You may print the final loadsheet if desired.


6. THE LOADSHEET TAB

The Loadsheet tab on the OpsCtrl GUI lets you request modifications. Perhaps you want to move cargo forward or aft, or perhaps you want to bump some standby passengers. Clicking one of the Reset buttons modifies the actual ZFW and CG in PSX. If you manipulate the ZFW or CG sliders in PSX after accepting the final loadsheet, the OpsCtrl app assumes you want your manually entered numbers to be controlling, so it won't apply any randomization unless you his one of teh Reset buttons on the GUI. 


7. FEEDBACK HELPS ME

If you want to leave feedback for me in on the Aerowinx board, it would be appreciated, and I'll take all suggestions into consideration. 




