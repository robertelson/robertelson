

#This will Turn off your CPU Laptops Turbo Mode!! Have fun



[Unit]
Description=disable cpustopboost.service Intel-CPU
 
[Service]
ExecStart=/bin/sh -c "/usr/bin/echo 1 > \
/sys/devices/system/cpu/intel_pstate/no_turbo"
ExecStop=/bin/sh -c "/usr/bin/echo 0 > \
/sys/devices/system/cpu/intel_pstate/no_turbo"
RemainAfterExit=yes
 
[Install]
WantedBy=sysinit.target
EOF
