﻿This wix 5.0 installer installs AV-Bible-Addin for Microsoft Word, olong with the AV-Data-Manager http service.
Code-Signing:
Find the Code Signing Certificate in the User’s Personal Certificates store: You can do this by navigating to Certificates - Current User → Personal → Certificates.
Obtain the signing certificate’s SHA1 thumbprint: Double click on the Code Signing Certificate in the User’s Personal Certificates store, go to Details → Thumbprint, mark the whole string and use Ctrl + C to copy

signtool sign /sha1 <thumprint> /fd SHA256 /t http://timestamp.digicert.com AV-Addin-Wix5-Installer.msi
