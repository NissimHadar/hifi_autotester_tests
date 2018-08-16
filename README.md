# High Fidelity Auto-Tester Tests
This is a repository of tests and various files for the auto-tester.

Testing automatic tester
	1.	Clone the auto-tester tests repository - git clone https://github.com/NissimHadar/hifi_autotester_tests.git
		
	2.	Download installer from https://hifi-content.s3.amazonaws.com/nissim/autoTester/AutoTester-Installer.exe
	3.	Install auto-tester in a temporary folder
	
	4.	Run the auto-tester executable auto-tester.exe
	5.	Select Help->About from the menu
		Verify built on Aug 10 2018, 15:22:40
		
	6.	Select Create tab
		1.	Create test
			1.  Open console and change to the hifi_autotester_tests that has just been cloned
			2.	>cd tests
			3.	>dir /s /w *.png | find "File(s)"
				Verify total of 21 images (last line displayed)
			
			4.	Click Create button
			5.	When prompted for folder containing the test images, select the hifi_autotester_tests/testCreationImages folder
			6.	When prompted for the test root folder, select the hifi_autotester_tests/tests folder
			7.	>dir /s /w *.png | find "File(s)"
				Verify total of 29 images (8 images were added)
				
		2.	Create test outline
			1.	>dir
				Verify folder (the tests folder) contains just 2 subfolders (content and engine)
				
			2.	Click Create Tests Outline
			3.	When prompted, select the tests root folder
				Verify testsOutline.md file has been created
				Verify this file is the same as the file by the same name in the hifi_autotester_tests folder
				
		3.	Create MD
			1.	>cd tests\content\entity\zone\zoneEffects
			2.	>dir
				Verify folder contains exactly 6 files (test.js and ExpectedImage_00000.png through ExpectedImage_00005.png)
				
			3.	Click Create MD button
			4.	When prompted select the tests\content\entity\zone\zoneEffects folder
				Verify test.md has been created in the tests\content\entity\zone\zoneEffects folder
				Verify this file is the same as the file by the same name in the hifi_autotester_tests folder
				Open the test.md file in the tests\content\entity\zone\zoneEffects with a suitable MD viewer and verify
				that steps 2,4,6,8 and 10 each display an image, and that the image matches the text
				
			5.	Click Create MD button
			6.	When prompted select the tests\content\entity\zone folder
				Verify "Could not find test.js" message
				Verify no file created in tests\content\entity\zone folder
				==============================================================================
			
		4.	Create all MDs
			1.	cd back up to the tests root folder
			2.	>dir /s /w *.md | find "File(s)"
				Verify total of 5 files
				
			3.	Click Create all MD files
			4.	When prompted, select the tests root folder
			5.	>dir /s /w *.md | find "File(s)"
				Verify total of 11 files
		
		5.	Create auto
			1.	>cd content\entity\light\point\create
			2.	>dir
				Verify folder contains exactly 1 file (test.js)
				
			3.	Click Create testAuto button
			4.	When prompted select the tests\content\entity\light\point\create folder
				Verify testAuto.js script has been created in the tests\content\entity\light\point\create folder
				Verify this file is the same as the file by the same name in the hifi_autotester_tests folder

			5.	Click Create testAuto button
			6.	When prompted select the tests\content\entity\light\point folder
				Verify "Could not find test.js" message
				Verify no file created in tests\content\entity\light\point folder
				==============================================================================

		6.	Create all auto
		7.	Create recursive
		8.	Create all recursive
		[Perform]
	7.	Evaluate
	8.	TestRail
	9.	Windows
		
		
	Need
		2 folders with images
			creating tests
			evaluating tests
			
			image names must match scripts
			
		A tree of test.js scripts
		
		Therefore: top level folder with 3 subfolders:
			tests hierarchy
			images for creation
			images for evaluation
		