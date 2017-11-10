# hostapd-mod-openwrt
This version of hostapd is intended for openwrt chaos-calmer build.
It has following capabilities-

1. Extract mac_addr of AP and STA and forward it to the controller. IP of the controller is read from /etc/config/hostapd_info

Note: It creates a new tcp connection with the controller for every association request and tears it down after receiving response.

2. Measure total setup time required (starting from state: ADD_STA  to state: STA_AUTHORIZED) and dump it to /tmp/bar.txt


List of files modified-

src/ap/sta_info.c 

src/ap/ieee802_11.c 

hostapd/main.c

