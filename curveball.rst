CurveBall (CVE-2020-0601)
=========================

From what I heard on Security Now, the exploit happens because crypt32.dll is allowing people to supply their own arguments (?) to the elliptic curve encryption function.

The root certificate for this ECC vulnerability is found in the Trusted Root Certification Authorities folder in the certificate manager. It is called "Microsoft ECC Product Root Certificate Authority 2018"

Links
-----

To tell if your system is vulnerable, you can go to `https://curveballtest.com <https://curveballtest.com>`_.

Exploiting this requires a Windows 10 VM with some version before
`KB4528760 <https://support.microsoft.com/en-us/help/4528760/windows-10-update-kb4528760>`_ or 
`KB4534273 <https://support.microsoft.com/en-us/help/4534273/windows-10-update-kb4534273>`_.

Post on `medium
<https://medium.com/zengo/win10-crypto-vulnerability-cheating-in-elliptic-curve-billiards-2-69b45f2dcab6>`_ contains a useful explanation of ECC.

Here's a good post on how to disable automatic updates `https://www.windowscentral.com/how-stop-updates-installing-automatically-windows-10`_.

The existing POC: `https://github.com/ollypwn/CurveBall`_.
