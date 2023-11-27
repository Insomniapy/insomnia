# insomnia
import subprocess
import os

def clear_screen():
    os.system('cls' if os.name == 'nt' else 'clear')

def print_banner():
    banner = """
/***
 *                   /$$ /$$ /$$                               /$$                        
 *                  |__/| $$| $$                              |__/                        
 *     /$$$$$$/$$$$  /$$| $$| $$  /$$$$$$  /$$$$$$$  /$$$$$$$  /$$ /$$   /$$ /$$$$$$/$$$$ 
 *    | $$_  $$_  $$| $$| $$| $$ /$$__  $$| $$__  $$| $$__  $$| $$| $$  | $$| $$_  $$_  $$
 *    | $$ \ $$ \ $$| $$| $$| $$| $$$$$$$$| $$  \ $$| $$  \ $$| $$| $$  | $$| $$ \ $$ \ $$
 *    | $$ | $$ | $$| $$| $$| $$| $$_____/| $$  | $$| $$  | $$| $$| $$  | $$| $$ | $$ | $$
 *    | $$ | $$ | $$| $$| $$| $$|  $$$$$$$| $$  | $$| $$  | $$| $$|  $$$$$$/| $$ | $$ | $$
 *    |__/ |__/ |__/|__/|__/|__/ \_______/|__/  |__/|__/  |__/|__/ \______/ |__/ |__/ |__/
 *                                                                                        
 *                                                                                        
 *                                                                                        
 */
    """

    print(banner)

print_banner()

print("Mac_Changer Started!")


subprocess.call(["ifconfig", "eth0", "down"])
subprocess.call(["ifconfig", "eth0", "hw", "ether", "00:22:22:44:77:99"])
subprocess.call(["ifconfig", "eth0", "up"])

