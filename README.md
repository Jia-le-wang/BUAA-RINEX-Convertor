The main function of this program is to convert multi-frequency and multi-constellation GNSS raw data collected by your own Android smartphones (such as Xiaomi Mi8, Huawei P40/Mate40, Samsung S20U, Google Pix6/Pix5a, OnePlus, Honor, etc.) into standard RINEX files. The program supports conversion of three - and four-frequency GNSS raw measurements to RINEX 3.05 observations.

-----------------------------------------------------------------------------------------------------
If you don't want to compile code, two quick ways to start are as follows:

1. Put all gnsslog.txt files in a folder with Gnsslogger2RINEX.exe, then double-click Gnsslogger2RINEX.exe to achieve batch conversion (please note: no Spaces in the path)

2. Alternatively, put all gnsslog.txt files in the same folder (such as TXTfiles) and use cmd or powershell to execute the following command:

Gnsslogger2RINEX.exe  C:\Users\Administrator\TXTfiles

------------------------------------------------------------------------------------------------------

Note that this program is different from the RINEX 3.04 file output from Google gnsslogger. BUAA-RINEX-Convertor aligns the time scale at all sampling times, which means that the sampling interval is equal 1s, rather than 0.999 s or 1.001 s. This avoids the inconsistency between the time difference of pseudorange/carrier phase and Doppler velocity measurement.


This program can batch process GNSS logs from Google gnsslogger (https://play.google.com/store/apps/details?id=com.google.android.apps.location.gps.gnsslogger&hl=en&gl=US) and GPSTEST (https://play.google.com/store/apps/details?id=com.android.gpstest&hl=en&gl=US). For information on whether the smartphone you are using supports GNSS raw measurements (pseudorange, carrier, Doppler, single/dual frequency, etc.) please refer to: https://docs.google.com/spreadsheets/d/1jXtRCoEnnFNWj6_oFlVWflsf-b0jkfZpyhN-BXsv7uo/edit#gid=0. The original version of the program came from Gao Yang's group at the University of Calgary, Thank them for their hard work and sharing. On the basis of their work. This program modifies some parameter errors and adds batch processing, Beidou/QZSS dual/multi frequency and other functions.

------------------------------------------------------------------------------------------------------
![-cropped-ezgif com-optimize (1)](https://github.com/Jia-le-wang/BUAA-RINEX-Convertor/assets/49149409/5dcc11a4-6d18-48bf-9ee6-2b1d8c64be0d)

------------------------------------------------------------------------------------------------------
Finally, IMU data processing (noise reduction, interpolation, time synchronization) is also very important if you want to further study the GNSS/SINS integrated navigation algorithm. We have completed this work and will upload the corresponding program later.

If you have any questions, please do not hesitate to contact me at: wangjialea@gmail.com
