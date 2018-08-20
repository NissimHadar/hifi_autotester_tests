# High Fidelity Auto-Tester Tests
This is a repository of tests and various files for the auto-tester.

## Testing automatic tester
**General**
1. Clone the auto-tester tests repository - git clone https://github.com/NissimHadar/hifi_autotester_tests.git
		
1. Download installer from https://hifi-content.s3.amazonaws.com/nissim/autoTester/AutoTester-Installer.exe
1. Install auto-tester in a temporary folder
	
1. Run the auto-tester executable auto-tester.exe
2. Select Help->About from the menu
   Verify built on Aug 20 2018, 10:44:44
   
1. Click Close
   Verify auto-tester closes cleanly
   
1. Run the auto-tester executable auto-tester.exe		
**Create test**
1. Select Create tab (the default)
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
	 Verify folder (the tests folder) contains just 2 subfolders (content and engine)
				
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
**Evaluate**
1. Create an empty folder for snapshots
1. Run Interface
1. Select this folder for snapshots (Settings->General)
2. Enter your local sandbox (so you can create entities)
3. Go to an empty area
4. Run the `tests\testRecursive.js` script (created in the previous step)
   Verify 29 images have been created in the snapshots folder
	8.	TestRail
	9.	Windows		