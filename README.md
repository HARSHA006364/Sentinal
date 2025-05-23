# Sentinal
import streamlit as st
import json
# your other imports

def scan_files():
    # simulated scan logic
    return "No threats found!"

def check_privacy():
    # simulated privacy check logic
    return "Camera and location access are safe."

def check_website(url):
    # simulated phishing check
    if "phishing" in url:
        return "Warning: This site might be phishing."
    return "Site looks safe."

def main():
    st.title("Sentinal Security Agent")
    user_input = st.text_input("Enter command")

    if user_input == "scan files":
        st.write(scan_files())
    elif user_input == "check privacy":
        st.write(check_privacy())
    elif user_input.startswith("check website"):
        url = user_input.split(" ")[2]
        st.write(check_website(url))
    else:
        st.write("Unknown command.")

if __name__ == "__main__":
    main()

