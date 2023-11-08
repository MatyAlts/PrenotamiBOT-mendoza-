# <img src="https://github.com/MatyAlts/PrenotamiBOT-mendoza-/blob/main/tito_icon.png" width="25" title="hover text"> TITO FOR MENDOZA
tito is a bot used to book a day to request italian citizenship (by any method) or passport at Prenot@Mi website.

It's coded in Python, with the Selenium package for web scraping.

### Usage:

1. Clone this repository in your computer. For this, open a Git bash, navigate to the directory where you want the cloned repository to be added, and copy&paste the following command:
```
$ git clone https://github.com/hvignolo87/tito.git
```

2. Fill in **user_data.ini** the **email**, **pass** and **service** fields with your data, then go to the selected service section and fill the form data. Also fill the **otp_delay** parameter (see point 5 below). For example:
```
[PRENOTAMI_DATA]
email = johndoe@gmail.com
pass = JohnDoe
service = anagrafe
otp_delay = 10

[ANAGRAFE]
NOTES = This is a note for the embassy.
```

3. Open a CLI (bash, powershell) and navigate to the **BOT** folder with the *cd* command. Once there, copy&paste the following command:
```
python main.py
```

4. Depending on the selected service, the script runs until the OTP code is required (this depends on the location of the selected embassy). Once the popup window shows, you need to enter it manually. **Don't click OK once inserted the code, just wait**.
You'll need to play with the *otp_delay* parameter in order to adjust it as minimum as possible. Start with 10s.

5. Enjoy.

## Future improvings
- [x] Develop a user-friendly web interface with Flask.
- [ ] Automate the OTP code insertion.
- [ ] Evaluate real time response, with high traffic in the website, in order to improve performance.
