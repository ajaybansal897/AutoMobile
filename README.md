using System;
using System.Text;
using System.Text.RegularExpressions;
using System.Threading;
using NUnit.Framework;
using OpenQA.Selenium;
using OpenQA.Selenium.Firefox;
using OpenQA.Selenium.Support.UI;


namespace SeleniumTests
{
    [TestFixture]
    public class VerifyJDPowerLinkClickMakeModelYearExpectedJDPowerWebpagedisplayed
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "https://www.katalon.com/";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheVerifyJDPowerLinkClickMakeModelYearExpectedJDPowerWebpagedisplayedTest()
        {
            driver.Navigate().GoToUrl("http://localhost/Automobile/index.php");
            driver.FindElement(By.LinkText("New")).Click();
            driver.FindElement(By.Id("sname")).Click();
            driver.FindElement(By.Id("sname")).Click();
            driver.FindElement(By.Id("sname")).Clear();
            driver.FindElement(By.Id("sname")).SendKeys("Harry");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Seller Name'])[1]/following::label[1]")).Click();
            driver.FindElement(By.Id("address")).Click();
            driver.FindElement(By.Id("address")).Clear();
            driver.FindElement(By.Id("address")).SendKeys("123 hILTON PARK");
            driver.FindElement(By.Id("city")).Click();
            driver.FindElement(By.Id("city")).Clear();
            driver.FindElement(By.Id("city")).SendKeys("Burlington");
            driver.FindElement(By.Id("pnumber")).Click();
            driver.FindElement(By.Id("pnumber")).Clear();
            driver.FindElement(By.Id("pnumber")).SendKeys("4785963210");
            driver.FindElement(By.Id("email")).Click();
            driver.FindElement(By.Id("email")).Clear();
            driver.FindElement(By.Id("email")).SendKeys("harry@gmail.com");
            driver.FindElement(By.Id("vmake")).Click();
            driver.FindElement(By.Id("vmake")).Clear();
            driver.FindElement(By.Id("vmake")).SendKeys("Honda");
            driver.FindElement(By.Id("model")).Click();
            driver.FindElement(By.Id("model")).Clear();
            driver.FindElement(By.Id("model")).SendKeys("Civic");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Model'])[1]/following::label[1]")).Click();
            driver.FindElement(By.Id("year")).Click();
            driver.FindElement(By.Id("year")).Clear();
            driver.FindElement(By.Id("year")).SendKeys("2018");
            driver.FindElement(By.Id("nextBtn")).Click();
            driver.FindElement(By.LinkText("Civic,2018,Honda")).Click();
            Assert.AreEqual("2018 Honda Ratings, Reviews and Awards", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Change Make'])[1]/following::span[3]")).Text);
            Assert.AreEqual("", driver.Title);
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }
    }
}

namespace SeleniumTests
{
    [TestFixture]
    public class VerifyResetbtnClickExpectedFiledsshouldgetcleared
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "http://localhost/Automobile/index.php#myPage";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheVerifyResetbtnClickExpectedFiledsshouldgetclearedTest()
        {
            driver.Navigate().GoToUrl("http://localhost/Automobile/index.php");
            driver.FindElement(By.LinkText("New")).Click();
            driver.FindElement(By.Id("sname")).Click();
            driver.FindElement(By.Id("sname")).Clear();
            driver.FindElement(By.Id("sname")).SendKeys("JD Power");
            driver.FindElement(By.Id("address")).Click();
            driver.FindElement(By.Id("address")).Clear();
            driver.FindElement(By.Id("address")).SendKeys("401 west highway");
            driver.FindElement(By.Id("city")).Click();
            driver.FindElement(By.Id("city")).Clear();
            driver.FindElement(By.Id("city")).SendKeys("Cambridge");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='City'])[1]/following::label[1]")).Click();
            driver.FindElement(By.Id("pnumber")).Click();
            driver.FindElement(By.Id("pnumber")).Clear();
            driver.FindElement(By.Id("pnumber")).SendKeys("1425367890");
            driver.FindElement(By.Id("email")).Click();
            driver.FindElement(By.Id("email")).Clear();
            driver.FindElement(By.Id("email")).SendKeys("jd@yahoo.com");
            driver.FindElement(By.Id("vmake")).Click();
            driver.FindElement(By.Id("vmake")).Clear();
            driver.FindElement(By.Id("vmake")).SendKeys("Suzuki");
            driver.FindElement(By.Id("resetBtn")).Click();
            Assert.AreEqual("", driver.FindElement(By.Id("sname")).Text);
            Assert.AreEqual("", driver.FindElement(By.Id("address")).Text);
            Assert.AreEqual("", driver.FindElement(By.Id("city")).Text);
            Assert.AreEqual("", driver.FindElement(By.Id("pnumber")).Text);
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }
    }
}

namespace SeleniumTests
{
    [TestFixture]
    public class VerifySavedDataClickSearchlinkExpectedAllSavedDatashoulddisplay
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "https://www.katalon.com/";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheVerifySavedDataClickSearchlinkExpectedAllSavedDatashoulddisplayTest()
        {
            driver.Navigate().GoToUrl("http://localhost/Automobile/index.php");
            driver.FindElement(By.LinkText("Search")).Click();
            Assert.AreEqual("1118 Kingstreet east", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Ajay'])[1]/following::td[1]")).Text);
            Assert.AreEqual("Ajay", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='make model year'])[1]/following::td[1]")).Text);
            Assert.AreEqual("Cambridge", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Ajay'])[1]/following::td[2]")).Text);
            Assert.AreEqual("4379822510", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Cambridge'])[1]/following::td[1]")).Text);
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }
    }
}
namespace SeleniumTests
{
    [TestFixture]
    public class VerifySubmitbtnEnterDetailsClicksubmitExpectedDatasaved
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "https://www.katalon.com/";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheVerifySubmitbtnEnterDetailsClicksubmitExpectedDatasavedTest()
        {
            driver.Navigate().GoToUrl("http://localhost/Automobile/index.php");
            driver.FindElement(By.LinkText("New")).Click();
            driver.FindElement(By.Id("sname")).Click();
            driver.FindElement(By.Id("sname")).Clear();
            driver.FindElement(By.Id("sname")).SendKeys("Adam");
            driver.FindElement(By.Id("address")).Clear();
            driver.FindElement(By.Id("address")).SendKeys("789 blue street");
            driver.FindElement(By.Id("city")).Clear();
            driver.FindElement(By.Id("city")).SendKeys("Milton");
            driver.FindElement(By.Id("pnumber")).Clear();
            driver.FindElement(By.Id("pnumber")).SendKeys("1239874560");
            driver.FindElement(By.Id("email")).Click();
            driver.FindElement(By.Id("email")).Clear();
            driver.FindElement(By.Id("email")).SendKeys("adam23@yahoo.com");
            driver.FindElement(By.Id("vmake")).Click();
            driver.FindElement(By.Id("vmake")).Clear();
            driver.FindElement(By.Id("vmake")).SendKeys("Hyundai");
            driver.FindElement(By.Id("model")).Clear();
            driver.FindElement(By.Id("model")).SendKeys("Sonata");
            driver.FindElement(By.Id("year")).Clear();
            driver.FindElement(By.Id("year")).SendKeys("2017");
            driver.FindElement(By.Id("nextBtn")).Click();
            Assert.AreEqual("Your Data", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Home'])[1]/following::h2[1]")).Text);
            // ERROR: Caught exception [unknown command []]
            // ERROR: Caught exception [unknown command []]
            // ERROR: Caught exception [unknown command []]
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }
    }
}
