# phantomjs-driver
phantomjs-driver for selenim whit 4.0.0

Test code:
```java
public static void main(String[] args) throws MalformedURLException {
        System.setProperty("phantomjs.binary.path", "/usr/local/Caskroom/phantomjs/2.1.1/phantomjs-2.1.1-macosx/bin/phantomjs");
        DesiredCapabilities caps = new DesiredCapabilities();
        caps.setBrowserName("chrome");
        caps.setJavascriptEnabled(true);
        caps.setCapability("takesScreenshot", true);
        WebDriver driver = new PhantomJSDriver(caps);
        driver.get("https://detail.1688.com/offer/640789245623.html");
        System.out.println(driver.getTitle());
        driver.quit();
    }
