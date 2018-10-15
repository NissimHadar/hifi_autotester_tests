# High Fidelity Auto-Tester Tests
This is a repository of tests and various files for the auto-tester.

## Testing automatic tester
**General**
1. Clone the auto-tester tests repository - git clone https://github.com/NissimHadar/hifi_autotester_tests.git
		
1. Download installer from https://hifi-content.s3.amazonaws.com/nissim/autoTester/AutoTester-Installer-v6.6.exe
If Windows message "Windows protected your PC" message appears, don't believe it.  Click "More info", then "Run anyway".

1. Install auto-tester in a temporary folder
	
1. Run the auto-tester executable auto-tester.exe
2. Select Help->About from the menu
   Verify built on Oct 10 2018, 15:29:14
1. Click OK to close About window
   
1. Click Close  
   Verify auto-tester closes cleanly
   
1. Run the auto-tester executable auto-tester.exe		
## GitHub Fields
**Default values**
1. Verify GitHub User default is `highfidelity`
1. Verify GitHub Branch default is `master`
**Enabling**
3. Verify `Create` tab is the default
4. Verify GitHub fields disabled
5. Select Windows tab
6. Verify GitHub fields disabled
7. Select Run tab
8. Verify GitHub fields enabled
9. Select Evaluate tab
10. Verify GitHub fields enabled
11. Select TestRail tab
12. Verify GitHub fields disabled
## Create
**Create test**
1. Select Create tab
1. Open a console and change directory to the hifi_autotester_tests that has just been cloned
1. `cd tests`
1. `dir /s /w *.png | find "File(s)"`
		Verify total of 21 images (last line displayed)
			
1. Click Create Tests button
1. When prompted for folder containing the test images, select the hifi_autotester_tests/testCreationImages folder
1. When prompted for the test root folder, select the hifi_autotester_tests/tests folder
1. `dir /s /w *.png | find "File(s)"`
Verify total of 29 images (8 images were added)
1. Click Create Tests button
1. When prompted for folder containing the test images, click Cancel
   Verify no error messages
				
**Create test outline**
1. Make sure you are in the tests folder
1. `dir`
	 Verify folder (the tests folder) contains just 3 subfolders (content, engine and utils)
				
1. Click Create Tests Outline button
1. When prompted, select the tests root folder
	 Verify testsOutline.md file has been created
	 Verify this file is the same as the file by the same name in the hifi_autotester_tests folder
	 
1. Click Create Tests Outline button
1. When prompted, click Cancel
   Verify no error messages. 
**Create MD**
1. `cd tests\content\entity\zone\zoneEffects`
1. `dir`
   Verify folder contains exactly 6 files (test.js and ExpectedImage_00000.png through ExpectedImage_00005.png)
				
1. Click Create MD button
1. When prompted select the tests\content\entity\zone\zoneEffects folder
   Verify test.md has been created in the tests\content\entity\zone\zoneEffects folder
	 Verify this file is the same as the file by the same name in the hifi_autotester_tests folder
	 Open the test.md file in the tests\content\entity\zone\zoneEffects with a suitable MD viewer and verify that steps 2,4,6,8 and 10 each display an image, and that the image matches the text
				
1. Click Create MD button
1. When prompted select the tests\content\entity\zone folder
   Verify "Could not find test.js" message
   Verify no file created in tests\content\entity\zone folder
   
1. Click Create MD button
1. When prompted, click Cancel
   Verify no error messages
   
**Create all MDs**
1. Change directory back up to the tests root folder
1. `dir /s /w *.md | find "File(s)"`
   Verify total of 6 files
				
1. Click Create all MD files button
1. When prompted, select the tests root folder
1. `dir /s /w *.md | find "File(s)"`
   Verify total of 12 files
   
1. Click Create all MD files button
1. When prompted, click Cancel
   Verify no error messages
   
**Create auto**
1. Click Create testAuto script button
1. When prompted, click Cancel
   Verify no error messages
   
1. `cd content\entity\light\point\create`
1. `dir`
   Verify folder contains exactly 3 files
				
1. Click Create testAuto script button
1. When prompted select the tests\content\entity\light\point\create folder
   Verify testAuto.js script has been created in the tests\content\entity\light\point\create folder
   Verify this file is the same as the file by the same name in the hifi_autotester_tests folder
   
1. Click Create testAuto button
1. When prompted select the tests\content\entity\light\point folder
   Verify "Could not find test.js" message
   Verify no file created in tests\content\entity\light\point folder
   
**Create all auto**
1. Change directory back up to the tests root folder
1. `dir /s /w testAuto.js | find "File(s)"`
   Verify total of 3 files
        
1. Click Create all testAuto scripts button
1. When prompted, select the tests root folder
1. `dir /s /w testAuto.js | find "File(s)"`
   Verify total of 9 files
   
1. Click Create all testAuto scripts button
1. When prompted, click Cancel
   Verify no error messages
   
**Create recursive**
1. `cd content\entity\light\point\create`
1. `dir`
   Verify folder contains exactly 4 files
        
1. Click Create Recursive Script button
1. When prompted select the tests\content\entity\light\point\create folder
   Verify testRecursive.js script has been created in the tests\content\entity\light\point\create folder
   Verify this file is the same as the file **testRecursive1.js** in the hifi_autotester_tests folder

1. Click Create Recursive Script button
1. When prompted select the tests\content\entity\light folder
   Verify testRecursive.js script has been created in the tests\content\entity\light folder
   Verify this file is the same as the file **testRecursive2.js** in the hifi_autotester_tests folder
   
1. Click Create Recursive Script button
1. When prompted, click Cancel
   Verify no error messages
   
**Create all recursive tests**
1. Change directory back up to the tests root folder
1. `dir /s /w testRecursive.js | find "File(s)"`
   Verify total of 4 files
  
1. Click Create all Recursive Scripts button
1. When prompted, select the tests root folder
1. `dir /s /w testRecursive.js | find "File(s)"`
   Verify total of 15 files
   Verify testRecursive.js script has been created in the tests folder
   Verify this file is the same as the file **testRecursive3.js** in the hifi_autotester_tests folder
   
1. Click Create all Recursive Scripts button
1. When prompted, click Cancel
   Verify no error messages
## Run
1. Create an empty folder
1. Verify Run Now button is disabled
1. Click Select Working Folder and choose the folder just created
   Verify Run button is now enabled
3. Verify Server-less check-box is unchecked
4. Verify Run latest check-box is checked
4. Click Run Now and wait 30 minutes
5. Verify the folder that was created now contains a file named `log.txt` (among others)
   Verify that this (text) file contains 2 lines, similar to the following:
```Tests started at 15:20, on Fri, Sep 21, 2018```
```Tests completed at 15:43, on Fri, Sep 21, 2018; 6 failures```

7. Verify the folder that was created now contains 2 Folders:  `High Fidelity` and `snapshots`
8. Verify that the `snapshots` folder contains a single zip file, named `TestResults--####-##-##_##-##-##(####).zip`
## Evaluate
**Evaluate**
1. Select the Evaluate tab in auto-tester
3. Verify Interactive Mode check-box is selected (this is the default)
4. Click Evaluate Test
5. When prompted for test images folder, Click Cancel
   Verify no error messages
   
1. Click Evaluate Test
2. When prompted for test images folder, select hifi_autotester_tests/testEvaluationImages_good
   Verify "All images are as expected message
   Verify an empty zipped folder has been created in hifi_autotester_tests/testEvaluationImages_good (named TestResults--####-##-##_##-##-##(####).zip:  The build number in parentheses)
   
1. Click Evaluate Test
2. When prompted for test images folder, select hifi_autotester_tests/testEvaluationImages_bad
   Verify failure
   
3. Click "Abort current test"
   Verify "One or more images are not as expected" message
  
1. Click Evaluate Test
2. When prompted for test images folder, select hifi_autotester_tests/testEvaluationImages_bad
   Verify failure
   
1. Click "Fail"
   Verify second failure appears
   
1. Click "Pass"
   Verify third failure appears
   
1. Click "Fail"
   Verify "One or more images are not as expected" message
   Verify a second zipped folder has been created in hifi_autotester_tests/testEvaluationImages_bad
   Verify this folder has two sub-folders, one for each failure
   
1. Clear "Interactive Mode" Check-box
1. Click Evaluate Test
2. When prompted for test images folder, select hifi_autotester_tests/testEvaluationImages_bad
   Verify "One or more images are not as expected" message
   Verify a third zipped folder has been created in hifi_autotester_tests/testEvaluationImages_bad
   Verify this folder has three sub-folders, one for each failure
   Verify that the content of the third folder is identical to the folder of the same name in the hifi_autotester_tests folder.
## TestRail
**Create Test Cases**
1. Create a temporary folder for the following tests
1. Select TestRail tab
2. Select XML radio button (default is Python)
3. Click "Create Test Cases"
4. When prompted, select the tests root folder
   Verify a file named "TestRailSuite.xml" has been created
   Verify this file is identical to the file of the same name in the hifi_autotester_tests folder
   
1. In a browser, go to <https://highfidelity.testrail.net/index.php?/suites/view/1311>
2. Click the Import Cases icon![](./ImportCasesIcon.png)
3. Select "Import from XML"
4. Click "Choose File" and select the XML file just created
5. Click Import
   Verify that a test suite has been created (note the time tag in the section name).
   The sections should match the folder layout in hifi_autotester_tests/tests
6. Delete the XML file
7. Select the Python radio button
8. Click "Create Test Cases"
9. When prompted, select the tests root folder
10.  When prompted, select the temporary folder
11. In the TestRail Run Selector Window, enter your TestRail user and password
12. Change the TestRailSuite ID from 1312 to 1311
13. Click "Accept"
14. After the "TestRail Added fro Release" combo has been populated, click "OK"
15. When prompted to run the script, click "Yes"
16. Wait for the "Updating..." window to close
17. Browse to <https://highfidelity.testrail.net/index.php?/suites/view/1311&group_by=cases:section_id&group_order=asc>
    Verify a new main section has been added (note the time tag in the section name)
    The sections should match the folder layout in hifi_autotester_tests/tests
    
**Create Run**
1. Click "Create Run"
2. When prompted, select the temporary folder
3. In the TestRail Run Selector Window, enter your TestRail user and password
4. Change the TestRailSuite ID from 1312 to 1311
5. Click "Accept"
   Verify that the "TestRail Sections" combo is populated with the sections previously created
1. Click OK
2.  When prompted to run the script, click "Yes"
3. Wait for the "Updating..." window to close
4. Browse to <https://highfidelity.testrail.net/index.php?/runs/overview/26>
   Verify that a test run has been created.
   Verify that it is 0% complete
**Update Run results**
1. Click "Update Run Results"
2. When prompted, select the last zipped failure results folder, created in the Evaluation test (in  in hifi_autotester_tests/testEvaluationImages_bad)
3. When prompted, select the temporary folder
4. In the TestRail Run Selector Window, enter your TestRail user and password
4. Change the TestRailSuite ID from 1312 to 1311
5. Click "Accept"
   Verify that the "TestRail Run" combo is populated with the sections previously created
1. Select the last run that has been created (the run from the previous step)
7. Click OK
8.  When prompted to run the script, click "Yes"
9. Wait for the "Updating..." window to close
4. Browse to <https://highfidelity.testrail.net/index.php?/runs/overview/26> (if already open - refresh the page)
   Verify that 6 tests have passed, 3 failed and none untested
## Windows (only)
1. Select the Windows tab
2. Click "Hide Windows Taskbar"
   Verify windows taskbar is hidden
   
1. Click "Show Windows Taskbar"
   Verify windows taskbar is shown
   
1. Click "Hide Windows Taskbar"
   Verify windows taskbar is hidden

