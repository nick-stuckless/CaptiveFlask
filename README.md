# Custom CaptiveFlask Plugin Tutorial
A beginner-friendly walkthrough for building and testing captive portal plugins

This repository contains a simple, educational CaptiveFlask plugin designed for **WifiPumpkin3**.  
The goal is to help you understand how captive portals work, how CaptiveFlask renders templates, and how to safely test your own plugin in a controlled lab environment.

This tutorial is intentionally approachable — no prior experience with Flask or WifiPumpkin3 required.

---

## What you'll learn

- How captive portals intercept traffic on open Wi‑Fi networks
- How CaptiveFlask plugins are structured inside WifiPumpkin3
- How to build a custom login page using HTML and Flask routes
- How to test your plugin locally without exposing it to real users
- How template variables and form handling work inside CaptiveFlask

---

## Repository contents

salesforce/

  static/
  
    css/
    
      styles.css - Styling
      
    img/
    
      login-slack-close-fg.png - Salesforce logo
      
      logo214.svg - Salesforce logo
      

  templates/
  
    login.html - The login page rendered by CaptiveFlask
    
    login_successful.html - The login success page rendered by CaptiveFlask
    

  salesforce.py - The plugin logic (routes, rendering, form handling)
  salesforce.zip - All parts compressed and ready to go
  README.md  
  .gitattributes
---

## Getting started

### 1. Install WifiPumpkin3

git clone https://github.com/P0cL4bs/WiFi-Pumpkin.git  

cd WiFi-Pumpkin  

sudo python3 setup.py install  


### 2. Locate the CaptiveFlask plugin directory

~/.config/wifipumpkin3/captiveflask/plugins/


### 3. Drop in the custom plugin

cp -r CaptiveFlask/* ~/.config/wifipumpkin3/captiveflask/plugins/


### 4. Launch WifiPumpkin3

sudo wifipumpkin3

Then navigate to:

Modules → CaptiveFlask → Custom Plugin

Enable it and start your test access point.

---

## Safe testing in a lab environment

This tutorial is designed for **local, controlled testing only**. You can safely test your plugin by:

- Using a virtual machine connected to your test AP
- Running WifiPumpkin3 on an isolated network
- Observing how the captive portal behaves when a device joins

This helps you understand the mechanics of captive portals without interacting with real users or production networks.

---

## How the plugin works

### Template rendering

The plugin uses a simple Flask route to render the login page template.

### Form handling

Submitted form data is captured and logged locally for demonstration purposes.  
This shows how captive portals process user input, but **should only be used for educational testing**.

---

## Learning goals

This tutorial focuses on:

- Understanding captive portal flow
- Learning how Flask templates integrate with WifiPumpkin3
- Experimenting with custom HTML/CSS login pages
- Building confidence modifying and extending plugins

It is **not** intended for real‑world credential collection or unauthorized network activity. The use of Salesforce imagery is to illustrate the danger of MitM credential capture.

---

## Repository link

If you're viewing this README elsewhere, the full repo is here:

https://github.com/nick-stuckless/CaptiveFlask
