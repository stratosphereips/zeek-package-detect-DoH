# Goal
Detect DoH servers by adding a is_DoH field in ssl.log and add timeout to them so that the DoH connection won't take too long

Running Zeek using this script will result in a is_DoH column in ssl.log that is set to true if the destination IP is a DoH server


# Example 

This command

```bro -C -i wlp3s0 zeek-package-detect-DoH```

Will result in the following ```is_DoH``` column ssl.log

![ssl.log]( https://raw.githubusercontent.com/stratosphereips/zeek-package-detect-DoH/main/images/is_DoH_field.png )


The ```is_DoH``` value of IP ```64.20.34.50``` is set to ```T``` because it is a DoH server.
