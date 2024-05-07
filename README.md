# Features

- Retrieves the browser user agent from an HTTP request.

- Gets geolocation (country, region, city) from the IP address.

- Captures an image of the page visited by the user.

- Retrieves the HTML source code of the visited page.

- Extracts data from a specific input field on the page.
  
- Retrieves the cookies stored by the victim’s browser for the domain visited.

- Generates Cross-Site Scripting (XSS) payloads according to the specified type

- Generates text reports containing test results. ***The generate_report(findings) function*** organizes the findings by category to facilitate analysis.

 ***It is a tool intended for authorized security professionals to perform penetration tests with prior consent. The author of the script is not responsible for the use of the script for illegal purposes.***

# Installing
- Make sure you have Python 3.6 or higher installed.
  
- Clone the repository using the git clone https://github.com/mrfelpa/Colletor.git
  
- Navigate to the Sherlock project folder.
  
- Install the dependencies by running:

          pip install -r requirements.txt

# Exemplo de Uso

        from get_geolocation import get_geolocation
        from take_screenshot import take_screenshot
        
        target_ip = "0.0.0.0"  # Replace with real IP
        country, Region, city = get_geolocation(victim_ip)
        
        if country:
          print(f"Victim’s location: {country}, {Region}, {city}")
        he:
          print("Failed to get geolocation")
        
        target_url = "https://www.test.com"  # Replace with real URL
        take_screenshot(target_url)
        print(f"Screenshot saved in screenshot.png")

- The results are recorded in the log file (penetration_testing.log) and in the text report (penetration_testing_report.txt).
