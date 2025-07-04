# TASK-7-CYBERS-SECURITY-INTERSHIP
# Chrome Extension Audit (Browser Security Cleanup)

Browser extensions can enhance Chrome’s functionality (ad blocking, password managers, etc.), but they also pose security and privacy risks. Malicious or outdated extensions may inject ads, steal data, or slow down the browser. Chrome extensions often require broad permissions (access to browsing history, cookies, web page data, etc.), so a compromised add-on can expose credentials or browsing data.  Security experts therefore recommend regularly auditing your installed extensions and ensuring each one is trustworthy. This report outlines steps to audit Chrome extensions on Windows: how to view installed extensions, evaluate their safety, and disable or remove any that are unnecessary or suspicious.

## Viewing Installed Chrome Extensions

1. **Open Chrome’s Extensions page.** In Chrome on Windows, click the three-dot menu (⋮) at the top-right, then go to **More tools** ▶ **Extensions**. You can also enter `chrome://extensions` in the address bar. This opens a page listing all extensions installed in the browser.

2. **Inspect the list of add-ons.** On the Extensions page, each extension is shown with its name, icon, and an on/off toggle switch. Enabled extensions have the toggle turned on. You can click **Details** for any extension to see more information (permissions, site access, etc.). If you only want to disable an extension without uninstalling it, toggle it off here; the extension will remain installed but inactive.

3. **Note profiles and locations.** (If you use multiple Chrome profiles, repeat this for each profile.) The Extensions page shows every add-on tied to that profile. Take note of any extensions you don’t recognize or no longer use.

After this, you should have a clear view of every installed Chrome extension on the machine, along with which ones are currently active.

## Researching Extension Safety

For each installed extension, verify that it’s legitimate and safe:

* **Check the source and store.** Prefer extensions from the official Chrome Web Store or known developers. Chrome’s Enhanced Safe Browsing flags any extension whose publisher hasn’t followed Google’s Web Store policies. In practice, that means if an extension is on the Web Store and by a reputable company, it’s likely been reviewed. Be cautious of extensions installed outside the Web Store or from random websites (these often require “developer mode” in Chrome). Stick to “trusted” developers – as Google notes, about 75% of Web Store extensions are by developers who meet Google’s security criteria.

* **Review the developer and listing.** Look up the extension’s name and developer online. Examine the extension’s Web Store page or official site for a clear description of its purpose. Security blogs advise checking developer information: a well-known company or identifiable developer (with company name, contact info) is a good sign. Read the extension’s reviews and ratings in the Chrome Web Store. Reviews can reveal if other users encountered ads, redirects, or suspicious behavior. In fact, experts explicitly recommend “scrutiniz\[ing] reviews” and avoid lookalike extensions. If the reviews mention spyware, unexplained ads, or data leaks, treat the extension as suspicious. Conversely, a widely-used extension with many installs and positive reviews is generally safer.

* **Inspect requested permissions.** Click **Details** on the extension to see its permissions and the sites it can access. Be wary if an extension asks for very broad access (like “read and change all your data on all websites”). Good security practice is to question why an extension needs each permission. For example, if a tool’s main feature is purely cosmetic, it shouldn’t require access to every website you visit. Chrome lets you limit site access (you can allow an extension only on click, on specific sites, or on all sites). Review this carefully. If permissions seem excessive or unrelated to the extension’s function, this is a red flag. Always check permissions *before* installing or updating an extension; malicious updates often try to expand the permission scope during an upgrade.

* **Check extension updates and reviews.** On the Web Store page or via the Details panel, note when the extension was last updated. Extensions with frequent updates by the developer are generally better maintained (including security fixes). Also see if the developer has responded to user reports. Remember that ratings can be manipulated, so if most reviews are glowing but some report problems (and especially if negative reviews were removed), be cautious.

* **Trust your instincts – uninstall if unsure.** If you’re uncertain about what an extension does, or you find no reliable information about it, the safest choice is to remove it. Security guidance is clear: if you don’t recognize or need an extension, “you should uninstall it”. Even disabled extensions can sometimes be reactivated or exploited, so if an extension has no clear purpose or a dubious pedigree, remove it. In short, keep only the extensions you trust and use regularly.

## Removing or Disabling Extensions

After identifying any unwanted or suspicious extensions, remove or disable them:

1. **Disable an extension (optional).** On the Extensions page in Chrome (chrome://extensions), use the toggle switch to turn off an extension. This keeps it installed but inactive, so it cannot run or use permissions. Disabling is useful if you’re undecided and want to test whether Chrome runs fine without it.

2. **Uninstall the extension.** To remove an extension completely, click **Remove** on its card in the Extensions page. You will be asked to confirm; click **Remove** again. Alternatively, if the extension’s icon is visible in the toolbar, you can right-click the icon and choose **Remove from Chrome**. This deletes the extension from your browser. (If Chrome says an extension is “managed by your organization” and won’t let you remove it, you may need to use the Chrome Policy Remover tool or contact your admin. In most home setups, this won’t apply.)

3. **Restart Chrome.** After disabling or uninstalling extensions, quit and relaunch Chrome. Restarting ensures any background processes or injected scripts from those extensions are cleared. It also lets you verify Chrome’s performance and behavior without the removed extensions (if performance improves or errors disappear, that confirms you removed a culprit).

By the end of this process, any unneeded or risky extensions should be turned off or gone. Document which extensions you removed or kept, along with your reasons. If all installed extensions were from reputable sources and needed, you may find none need removal. In that case, simply note that all remaining extensions were verified as safe.

## Importance of Extension Audits

Regularly auditing browser extensions is critical for security and performance. Chrome extensions run with significant privileges: many can read and modify the data on web pages you visit, capture clipboard contents, or access cookies and login tokens. If a malicious or compromised extension is present, it could surreptitiously steal credentials, session cookies, browsing history, or other sensitive data.  For example, security researchers recently uncovered a campaign of fake Chrome extensions that “masquerade as benign utilities” but actually **exfiltrate data and execute code** behind the scenes. These trojanized extensions were configured to grab cookies, hijack sessions, inject ads, and even load attacker-controlled scripts on every website.

Even extensions that start out safe can become dangerous if their update mechanism is hijacked. In late 2024, attackers phished Chrome extension developers to push malicious updates. At least 35 Chrome extensions (over 2.6 million users) were compromised this way, with stolen code inserted to harvest users’ cookies and access tokens. As one security expert put it, “Browser extensions are the soft underbelly of web security,” since they often have “extensive permissions to sensitive user information”. Many organizations found that they didn’t even know which extensions were installed on endpoints, greatly increasing their risk.

Aside from security, unnecessary extensions can degrade performance. Each extension adds background processes and code that Chrome must load. As a result, too many or outdated extensions can slow down browsing and consume extra memory. For example, security bloggers note that unused extensions take up space and can make Chrome “run more slowly or unstably”. Keeping only essential, well-updated extensions reduces the “attack surface” and often noticeably improves speed and stability.

In summary, a routine extension audit prevents spyware/adware infections and data leaks, and also keeps Chrome running efficiently. By verifying each extension’s legitimacy and removing rogue add-ons, you significantly strengthen browser security and privacy.

## Security Takeaways

* **Minimize extensions.** Every extension is additional code that can be attacked. Keep only those you truly need. Unused extensions should be removed.
* **Install from trusted sources.** Use the Chrome Web Store or well-known developers. Chrome’s Enhanced Safe Browsing flags untrusted extensions. Avoid downloading extensions from random sites or without a clear provenance.
* **Review regularly.** Periodically revisit Chrome’s Extensions page and audit what’s installed. Google and security experts advise checking and understanding your extensions on a routine basis.
* **Check permissions.** Pay close attention to what access an extension requests. If it asks for broad permissions (like access to all website data) without a clear need, that’s suspicious. Only grant permissions you’re comfortable with, and use Chrome’s controls to limit site access.
* **Uninstall unneeded or questionable extensions.** Immediately remove any extension you don’t use or can’t verify. This is safer even if you “might not need it” later. Remember that disabled extensions can still be harmful if someone re-enables them, so removal is best when in doubt.
* **Keep Chrome and extensions updated.** Updates often include security fixes. Ensure Chrome is up-to-date, and rely on its auto-update feature for extensions (or manually update them). Well-maintained extensions with recent updates are generally safer.

