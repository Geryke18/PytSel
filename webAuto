from selenium import webdriver
import time
from selenium.webdriver.common.action_chains import ActionChains

# fullscreen
options = webdriver.ChromeOptions()
options.add_argument("--start-maximized")
browser = webdriver.Chrome(chrome_options=options)

# load page
browser.get("http://www.dongolom.hu/")
time.sleep(2)

# scroll to video and play
video = browser.find_element_by_xpath('//*[@id="vidi"]/iframe[3]')
video.location_once_scrolled_into_view
video.click()
time.sleep(2)

# click 4. menu
bio = browser.find_element_by_xpath('//*[@id="topmenu1"]/li[4]/a/h2')
hover1 = ActionChains(browser).move_to_element(bio)
hover1.perform()
time.sleep(1)
bio.click()
time.sleep(2)

# click facebook link
fblink = browser.find_element_by_id('fb')
hover2 = ActionChains(browser).move_to_element(fblink)
hover2.perform()
time.sleep(1)
fblink.click()

# change to the new window
browser.switch_to_window(browser.window_handles[-1])

def fbLog():
    # fill input fields
    user = browser.find_element_by_css_selector('#email')
    user.send_keys('example@gmail.com')
    password = browser.find_element_by_css_selector('#pass')
    password.send_keys('********')

    # click Log In button
    login = browser.find_element_by_css_selector('#u_0_2')
    login.click()

fbLog()
