MazelPrime Technologies Pvt. Ltd. - Website

index.html and thank-you.html are self-contained (logo and images are built in).

DEPLOY ON NETLIFY
  1. Drag THIS folder (the one that directly contains index.html) onto
     https://app.netlify.com/drop  -- not the folder above it.
  2. Site configuration > Forms > Enable form detection.
  3. Deploys > Trigger deploy > Deploy site  (forms are only detected on a new deploy)
  4. Forms > Form notifications > Add notification > Email > mazelprime9@gmail.com

TEST
  Submit the form on the live site -> you should land on thank-you.html and see
  the entry under Forms > discovery in Netlify.

LOCAL
  Opening index.html from your computer: the form skips sending and goes straight
  to thank-you.html (nothing is sent when not hosted).
