"""
Joe Wong Internal Operations
Etsy Open API v3 Sales Data Test Script
Personal use only - for learning and development purposes
"""

import requests

# Etsy API base URL
BASE_URL = "https://openapi.etsy.com/v3"

def test_public_endpoint():
    """Test a public Etsy API endpoint that doesn't require authentication"""
    endpoint = f"{BASE_URL}/application"
    
    # Replace with your actual API key when testing
    headers = {"x-api-key": "YOUR_API_KEY_HERE"}
    
    try:
        response = requests.get(endpoint, headers=headers)
        response.raise_for_status()
        print("Public API endpoint test successful!")
        print(f"Response status: {response.status_code}")
        print("\nNext step: Test authenticated sales data endpoints after OAuth authorization")
    except requests.exceptions.RequestException as e:
        print(f"API test failed: {e}")

if __name__ == "__main__":
    print("Testing Joe Wong Internal Operations - Etsy Open API v3 Sales Data")
    test_public_endpoint()
