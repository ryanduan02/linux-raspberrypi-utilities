# CPU Stress testing

1. Open terminal 1
2. run:
```bash 
watch -n 0.5 'printf "Fan state: "; cat /sys/class/thermal/cooling_device0/cur_state; printf "Temp: "; vcgencmd measure_temp'
```
3. You should see output like:
```text
Fan state: 0
Temp: temp=46.2'C
```
4. Install stress test tool:
```bash
sudo apt update
sudo apt install -y stress
```
5. Run stress test load on all CPU cores
`bash stress -c 4` (4 for me, but may vary)


   