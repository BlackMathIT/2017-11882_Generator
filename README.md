# CVE-2017-11882

A remote code execution vulnerability exists in Microsoft Office software when the software fails to properly handle objects in memory. An attacker who successfully exploited the vulnerability could run arbitrary code in the context of the current user.


# 2017-11882_Generator

This is a PoC re-edited, from the original one made by Embedi, to generate single file .rtf with a remote command execution embedded. 


## Usage

python 2017-11882_Generator.py -x command_to_execute -o output_file_name


WE ARE NOT RESPONSIBLE OF ANY DAMAGES CAUSED BY THE USE OF THIS SOFTWARE. 
IT WAS MADE FOR EDUCATIONAL PURPOSE AND TESTING ONLY!!!
