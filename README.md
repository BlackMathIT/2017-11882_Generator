# CVE-2017-11882

A remote code execution vulnerability exists in Microsoft Office software when the software fails to properly handle objects in memory. An attacker who successfully exploited the vulnerability could run arbitrary code in the context of the current user.


# 2017-11882_Generator

This is a PoC re-edited, from the original one made by Embedi, to generate single file .rtf with a remote command execution embedded. 


## Usage

python 2017-11882_Generator.py -x command_to_execute -o output_file_name

Example:
python 2017-11882_Generator.py -x "cmd /c calc" -o test.rtf

## Mitigation

For 32-bit Microsoft Office package in x86 OS:
reg add "HKLM\SOFTWARE\Microsoft\Office\Common\COM Compatibility\{0002CE02-0000-0000-C000-000000000046}" /v "Compatibility Flags" /t REG_DWORD /d 0x400

For 32-bit Microsoft Office package in x64 OS:
reg add "HKLM\SOFTWARE\Wow6432Node\Microsoft\Office\Common\COM Compatibility\{0002CE02-0000-0000-C000-000000000046}" /v "Compatibility Flags" /t REG_DWORD /d 0x400

## Patch 

Microsoft released a Patch
https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2017-11882

WE ARE NOT RESPONSIBLE OF ANY DAMAGES CAUSED BY THE USE OF THIS SOFTWARE. IT WAS MADE FOR EDUCATIONAL PURPOSE AND TESTING ONLY!!!
---------------------


www.blackmath.it | info@blackmath.it

