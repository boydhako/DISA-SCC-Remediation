# DISA-SCC-Remediation
This repo is primarily addressed to DISA SCC SCAP scan results for Red Hat Enterprise Linux (RHEL).

## Predicted Questions
- Why not use OpenSCAP/Foreman?
	- I have yet to work with Information Assurance (IA) and ATO personnel that would accept OpenSCAP assesments and/or results. SCC is the only *approved* security scanner that is recognized.
	- SCC isn't as compliant to SCAP 1.2 with the additional options like the remediation scripts that is found in OpenSCAP.
- If you're using the DISA STIG Security Profile, why do you need this?
	- The "Open" DISA STIG Security Profile is not complete in that it doesn't have the various specific profiles used for MAC levels and Sensitivity. It does however implement over 50% of the STIG implementations found by the SCC using the DISA Approved STIGs.

## STIG Priorities
1. Manual STIG Checks
	1. CAT I
	2. CAT II
	3. CAT III
2. SCC Benchmark Open Findings
	1. CAT I
	2. CAT II
	3. CAT III
3. SCC Benchmark Not A Findings
	1. CAT I
	2. CAT II
	3. CAT III

## Baseline Environment
1. Implemented DISA STIG Security Profile at install
	- Reduced need for updates to repo
2. Minimal basic installation
	- As services get enabled the STIG benchmarks change
3. BASH and SH as shell script interpreters
	- Minimal installation with only required software will not have "special" software available.
	- Basic standardized understanding of the language being used

## Philosophy
- Allow the scripts to be run multiple times efficiently with **ZERO** negative impact
- Allow the scripts to do perform standardized checks
- STIGs and software implementation constantly change. Therefore, checks and remediation should be assessed based on OS Minor versions.
- IA Auditors do not operate based off of CCI. The operate based off of Vulnerability IDs which is not a standard in SCAP standards.

## Strategy
( Flowchart is Work In Progress )
