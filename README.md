SSIS
====

<b>Description: </b> This process runs daily against SAP to provide Legal users with an update of the Invoices that have been processed the previous day. This process currently runs for three internal Legal functions and can have one of three results:
  1. Invoices are accounted for and their information is output into a file location as a XML file.
  2. There is a failure in one of the Invoices records in SAP and a .txt error file is output containing the Invoices that need to be fixed. 
  3. No Invoices are processed for the previous day and no output files are generated.
  
Depending on the result, an email containing the actions is sent to the appropriate business user.


<b>Below is an image of the SSIS Package<b/>
<img src="https://raw.github.com/nicholasceliano/SSIS/master/Images/SSISLayout.PNG" >

<b>Below is a peak into the Data Flow Tasks of the package</b>
<img src="https://raw.github.com/nicholasceliano/SSIS/master/Images/DataFlow_CompanyCode.PNG" >
<img src="https://raw.github.com/nicholasceliano/SSIS/master/Images/DataFlow_NoCompanyCodes.PNG" >
<img src="https://raw.github.com/nicholasceliano/SSIS/master/Images/DataFlow_OutputErrors.PNG" >

<b>Below is a snapshot of the File Location where all of the outputs are stored.</b>
<br />
- Test Outputs can be viewed under SSIS/Test Output/

<img src="https://raw.github.com/nicholasceliano/SSIS/master/Images/FileLocation.PNG" >
