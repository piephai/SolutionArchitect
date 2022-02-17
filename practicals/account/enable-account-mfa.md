# Enabling MFA for your account

1. On AWS console, click on your name on the top right hand corner and then click on "Security Credentials"

![profile-menu](../../images/iam/profile-menu.JPG)

2. Click on "Assign MFA Device"
   
   ![assign-mfa](../../images/iam/assign-mfa.JPG)

3. Select ```Virtual MFA``` however, if you were doing this in an actual production environment. It is recommended that you have a hardware MFA device
   
   ![viritual-mfa](../../images/iam/virtual-mfa.JPG)

4. Click to review the QR code and select the virtual MFA of your choice such as Microsoft Authenticator, Google Authenticator or Fortitoken. You will need to make sure that you enter the first code you see on your MFA app in the "MFA code 1" field and wait until your MFA app generates you a second code in which you will enter into the "MFA code 2" field. 

![mfa-qr-code](../../images/iam/mfa-qr-code.JPG)

5. Once you have set up your MFA you should see the screen below

![successful-mfa](../../images/iam/successful-mfa.JPG)