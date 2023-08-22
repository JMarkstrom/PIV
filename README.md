<h1 align="center"> YubiKey PIV "lifecycle" using Python</h1>

## ℹ️ About
The **yubikey-piv.py** script exemplifies how to use Python to perform YubiKey configuration and issuance of a PIV credential. 
With regards to issuance, the script creates a Certificate Signing Request (CSR) that, if issued, allows for authentication into Entra ID (Azure AD).
 
<sub>Configuring a YubiKey using Python (example):<sub>
![](/images/configure-yubikey.gif)

In summary, the script can perfor the following actions/tasks:

* Change Management Key
* Set a non-trivial(!) PIN
* Set a non-trivial(!) PUK
* Create a CSR
* Perform Attestation
* Import a certificate

⚠️ This script is provided "as-is" without any warranty of any kind, either expressed or implied.

## 💻 Prerequisites
You will need to meet the following prequisites to make use of this script:

- YubiKey Manager (get it [here](https://www.yubico.com/support/download/yubikey-manager/))
- One (1) YubiKey 5 series authenticator (with PIV support)
- An issuing Certificate Authority (CA) e.g a Microsoft PKI

## 📖 Usage
To use the [script](https://github.com/JMarkstrom/PIV/raw/main/yubikey-piv.py):

1. Simply open a command prompt and execute: ```ykman script yubikey-piv.py```
2. In the main menu, select an option and follow on-screen instructions.

Option ```1```: **Configure YubiKey**:

![](/images/configure-yubikey-piv-applet.gif)

Option ```2```: **Validate attestation**:

![](/images/validate-yubikey-attestation.gif)

Option ```3```: **import certifcate**:

![](/images/import-certificate-to-yubikey.gif)


**Note**: For more detail and broader context, please refer to [swjm.blog](https://swjm.blog)

## 🥅 Roadmap
Possible improvements includes:
- Separate CSR creation from YubiKey configuration (new menu option)
- Improve CSR to better match Microsoft domain and Entra ID requirements

## 🥷🏻 Contributing
Any help on the above (see roadmap) is welcome. 

## 📜 Release History
* 2023.08.15 `v1.2` minor improvements
* 2023.08.15 `v1.1` fixed spelling mistakes
* 2023.08.14 `v1.0` first release
