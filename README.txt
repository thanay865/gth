from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Edge()

driver.get("https://www.google.com/")
driver.maximize_window()

time.sleep(2)

search_box = driver.find_element(By.NAME, "q")
print("Search box found")

search_box.send_keys("Selenium Testing")

search_box.send_keys(Keys.RETURN)
print("Search executed")

time.sleep(3)

driver.quit()
