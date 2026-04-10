#!/bin/bash

clear
echo -e "\e[1;32m"
echo "  _   _  _______   _   _  ____      _____ _  _   "
echo " | \ | || ____\ \ / / | | / ___|    |___  | || |  "
echo " |  \| ||  _|  \ V /  | | \___ \ _____ / /| || |_ "
echo " | |\  || |___ /  \  | |_ ___) |_____/ / |__   _|"
echo " |_| \_||_____/_/ \_\  \__|____/     /_/     |_|  "
echo -e "\e[1;36m       Developed by: Mithilesh Dubey \e[0m"
echo "----------------------------------------------------"

echo "⏳ NEXUS-74 इंस्टॉल हो रहा है..."

pkg update -y
pkg install python tmux sqlite clang python-lxml -y
pip install pyTelegramBotAPI search-engine-parser ddgr wikipedia --no-deps

# आपका असली बॉट यहाँ से डाउनलोड होगा
curl -o ~/bot.py https://raw.githubusercontent.com/dmithilesh227-png/NEXUS-74/main/bot.py

# 'nexus' शॉर्टकट कमांड बनाना
echo "python ~/bot.py" > $PREFIX/bin/nexus
chmod +x $PREFIX/bin/nexus

echo -e "\e[1;32m✅ सेटअप पूरा हुआ! अब 'nexus' टाइप करें।\e[0m"
