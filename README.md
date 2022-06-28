For the purpose of confidentiality, the file code is protected. For the file password please email the code developer SERDESHT@GMAIL.COM.


The following describes how to use the code

****** 1 GENERATE BLAST OVER-PRESSURE PROFILE: RUN blast_loading_code.m, input parameters are the charge weight, scaled distance, and height of the sctructure. The parameters of blast-loading profiles are generated. The generated files which are used in the next step are supporting_file_blast_profile.tcl, supporting_file_pressure.tcl,and supporting_file_time.tcl.

****** 2 DETERMINISTIC ANALYSIS: OPEN analysis_main_body_file.tcl and run the .tcl to generate the structural response using the induced blast loading profile in the previous step.input parameters are the structural properties. Use input.tcl file for required data entry.

****** 3 PROBABILISTIC ANALYSIS: 3.1 Run the reliability_main_file_1st_step.m file, the file runs the redistribution file automatically ''redistribution_file_1st_step.m''. In this step 350 sample points are generated, which can be simply modified. Damage detection algorithm is embedded in this file to identify the failure The file also uses Latine-Hypercube-Sampling-Strategy to generate the random variables.

3.2 To determine the failure probability, run reliability_main_file_2nd_step.m. This file code produces the 10,000 sample points. In this file, plot fitting distribution is used to re-distribute the sample points in the previous step and use the best curve fitting parameters.

3.3 To run the sensitivity analysis, sensitive_parameters.m is used. Otherwise, using reference probabilistic modeling is sufficient.

3.4 The fragility analysis is performed by running the fragility_main_file_1st_step.m and fragility_main_file_2nd_step.m.

3.5 The results are created in the form of file.text in the created folder within the same directory

***** FOR ANY INQUIRY PLEASE CONTACT SERDESHT@GMAIL.COM or SARDASHT.SARDAR@EMK.BME.HU
