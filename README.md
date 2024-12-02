#!/bin/bash

# Print the WhatsApp logo
echo -e "\e[32m" # Set text color to green
echo "        .-\"\"\"\"\"\"-."
echo "      .'          '."
echo "     /   O      O   \\"
echo "    :           \`    :"
echo "    |                |"
echo "    :    .------.    :"
echo "     \\  '        '  /"
echo "      '.          .'"
echo "        '-......-'"
echo -e "\e[0m" # Reset text color

# Prompt for user input
echo "Direct WhatsApp message sender"
echo "Author: Arjun Singh"
echo -e "\n"

# Prompt for the sender's number (your friend's number)
read -p "Enter Sender's Country Code (without +): " sender_country_code
read -p "Enter Sender's WhatsApp number: " sender_num

# Prompt for the recipient's number (the other friend's number)
read -p "Enter Recipient's Country Code (without +): " recipient_country_code
read -p "Enter Recipient's WhatsApp number: " recipient_num

# Prompt for the message or link to send
read -p "Enter the message or link you want to send: " message

# Open WhatsApp with the recipient's number and custom message
echo "Opening WhatsApp on sender device..."
sleep 2
xdg-open "whatsapp://send?phone=$recipient_country_code$recipient_num&text=$message"
