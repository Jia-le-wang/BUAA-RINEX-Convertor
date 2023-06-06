The main function of this program is to convert dual-frequency and multi-constellation GNSS raw data collected by your own Android smartphones (such as Xiaomi Mi8, Huawei P40/Mate40, Samsung S20U, Google Pix6/Pix5a, OnePlus, Honor, etc.) into standard RINEX files.Note: Some of the latest smartphones such as Xiaomi Mi11, Huawei Mate40, HONOR 50, etc., support the Beidou triple frequency data (B1I+B1C+B2a). If you need, please share the data with me to increase the three-frequency data conversion function.

We evaluated the GNSS observations quality of different brands of smartphones in detail, and realized instantaneous sub-meter positioning based on dual-frequency smartphone PPP. For details, please refer to: https://doi.org/10.33012/navi.597 (Instantaneous Sub-meter Level Precise Point Positioning of Low-Cost Smartphones)

-------------------------------------------------------------------------------------------------------------
If you don't want to compile code, two quick ways to start are as follows:

1. Put all gnsslog.txt files in a folder with Gnsslogger2RINEX.exe, then double-click Gnsslogger2RINEX.exe to achieve batch conversion (please note: no Spaces in the path)

2. Alternatively, put all gnsslog.txt files in the same folder (such as TXTfiles) and use cmd or powershell to execute the following command:

Gnsslogger2RINEX.exe  C:\Users\Administrator\TXTfiles

-------------------------------------------------------------------------------------------------------------

The original version of the program came from Gao Yang's group at the University of Calgary. Thank them for their hard work and sharing: https://github.com/FarzanehZangeneh/csv2rinex. On the basis of their work, this program modifies some parameter errors and adds batch processing, Beidou /QZSS dual frequency and other functions.

Note that this program is different from the RINEX 3.04 file output from Google gnsslogger 3.0.5.6. GNSSLOG2RINEX aligns the time scale at all sampling times, which means that the sampling interval is equal 1s, rather than 0.999 s or 1.001 s. This avoids the inconsistency between the time difference of pseudorange/carrier phase and Doppler velocity measurement (this problem mainly exists in Huawei and Honor phones, which use two local clocks for the pseudorange and carrier phase instead of the usual one clock control).


This program can batch process GNSS logs from Google gnsslogger (https://play.google.com/store/apps/details?id=com.google.android.apps.location.gps.gnsslogger&hl=en&gl=US) and GPSTEST (https://play.google.com/store/apps/details?id=com.android.gpstest&hl=en&gl=US). For information on whether the smartphone you are using supports GNSS raw measurements (pseudorange, carrier, Doppler, single/dual frequency, etc.) please refer to: https://docs.google.com/spreadsheets/d/1jXtRCoEnnFNWj6_oFlVWflsf-b0jkfZpyhN-BXsv7uo/edit#gid=0


Finally, IMU data processing (noise reduction, interpolation, time synchronization) is also very important if you want to further study the GNSS/SINS integrated navigation algorithm. We have completed this work and will upload the corresponding program later.

If you have any questions, please do not hesitate to contact me at: wangjialea@gmail.com
