# SWE_2021_41_2024_2_week_6
------------------------------------------------------------------------------------------------------------------
Week4 Assignment
https://github.com/haein00-p/SWE_2021_41_2024_2_week_4.git
def isHappy(n):
  exist = set()
  while True:
    num = str(n)
    total = 0
    for i in num:
      total += int(i)**2
    if total in exist:
      return False
    elif total == 1:
      return True
    exist.add(total)
    n=total

  return

isHappy(input())

ºDescription
Make set named 'exist'. Then turn integer input to string.
Raise to the second power of each integer and sum them and save to total.
If that number already exists in set, it means that it is repeating, so that it is not a HappyNumber.
But if total is 1, it is HappyNumber, so it returns True.
If total is nor 1 neither in exist set, then total is added to exist set.
Then this total number turns to string, and this repetition continues until total is already in exist set or is 1.
\-------------------------------------------------------------------------------------------------------------------------
Week5 Assignment

ºdocker exec ossp-container cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
->command to get information about OS it is running based on the image of container.

ºdocker exec ossp-container git --version
git version 2.43.0
->command to check the version of git installed in container.

ºdocker exec ossp-container python3 --version
Python 3.12.3
->command to check the version of python installed in container.

ºdocker inspect --format="{{ .HostConfig.Binds }}" ossp-container
[/home/haein/ossp_host_dir:/mnt/ossp_container_dir]
->command to check the information of mount of container.


