- Severe powering troubles due to Micro USB power connector. It's recommended to [power through GPIO pins](https://forum.armbian.com/topic/3327-asus-tinkerboard/&do=findComment&comment=32047) to prevent under-voltage issues (instabilities, boot/crash cycles).
- Overclocking to 2.2GHz is possible with quality 3A PSU connected to GPIO pins and (patched) mainline kernel. Enable with:

		echo 1 > /sys/devices/system/cpu/cpufreq/boost		# enable turbo
		nano /etc/default/cpufrequtils 						# adjust new limit
		service cpufrequtils restart 						# restart cpufrequtils

