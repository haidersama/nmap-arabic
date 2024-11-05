# nmap-arabic
يركز هذا المستودع على تقديم اساسيات اداة (نماب)باللغة العربية للمبتدئين


### 1. **فحص بسيط**
   ```bash
   nmap <target>
   ```
   - فحص أساسي للهدف لتحديد المنافذ المفتوحة.

### 2. **فحص جميع المنافذ**
   ```bash
   nmap -p- <target>
   ```
   - فحص جميع المنافذ من 1 إلى 65535.

### 3. **كشف الخدمة والإصدار**
   ```bash
   nmap -sV <target>
   ```
   - يحدد الإصدار لكل خدمة تعمل على المنافذ المفتوحة.

### 4. **كشف نظام التشغيل**
   ```bash
   nmap -O <target>
   ```
   - يحدد نظام التشغيل على الجهاز المستهدف.

### 5. **فحص سريع**
   ```bash
   nmap -T4 <target>
   ```
   - فحص سريع باستخدام إعدادات "T4" لتسريع الفحص.

### 6. **فحص التخفي (SYN Scan)**
   ```bash
   nmap -sS <target>
   ```
   - فحص تخفي يستخدم حزم SYN.

### 7. **فحص UDP**
   ```bash
   nmap -sU <target>
   ```
   - فحص المنافذ التي تعمل على بروتوكول UDP.

### 8. **حفظ النتائج في ملف نصي**
   ```bash
   nmap -oN output.txt <target>
   ```
   - يحفظ نتائج الفحص في ملف نصي.

### 9. **حفظ النتائج بتنسيق XML**
   ```bash
   nmap -oX output.xml <target>
   ```
   - يحفظ النتائج بتنسيق XML لتحليلها لاحقًا.

### 10. **فحص الأجهزة الحية فقط**
   ```bash
   nmap -sn <target>
   ```
   - يكشف الأجهزة النشطة بدون فحص المنافذ.

### 11. **فحص نطاق شبكة كامل**
   ```bash
   nmap <network_range>
   ```
   - فحص كامل لنطاق شبكة مثل `192.168.1.0/24`.

### 12. **التخفي الكامل باستخدام فحص FIN**
   ```bash
   nmap -sF <target>
   ```
   - يستخدم حزم FIN لفحص المنافذ بشكل خفي.

### 13. **فحص باستخدام حزم Xmas**
   ```bash
   nmap -sX <target>
   ```
   - فحص خفي عبر حزم Xmas لجدران الحماية القديمة.

### 14. **فحص TCP Connect**
   ```bash
   nmap -sT <target>
   ```
   - يستخدم اتصال TCP كامل لفحص المنافذ المفتوحة.

### 15. **فحص بأسماء DNS**
   ```bash
   nmap -sL <network_range>
   ```
   - يحدد أسماء الأجهزة في نطاق IP.

### 16. **استخدام السكربتات للتحليل**
   ```bash
   nmap --script <script_name> <target>
   ```
   - يشغل سكربتات للتحقق من الثغرات والخدمات.

### 17. **فحص منافذ محددة**
   ```bash
   nmap -p <port_range> <target>
   ```
   - يحدد نطاقًا معينًا من المنافذ للفحص، مثل `1-1000`.

### 18. **تجاوز الحماية بفحص TCP ACK**
   ```bash
   nmap -sA <target>
   ```
   - يستخدم حزم ACK لتجاوز الجدران النارية.

### 19. **فحص NULL**
   ```bash
   nmap -sN <target>
   ```
   - فحص لا يرسل أي علامات TCP، لكشف المنافذ الخفية.

### 20. **فحص باستخدام حزم IP**
   ```bash
   nmap -sO <target>
   ```


---

### 21. **فحص أبطأ لتجنب اكتشافه**
   ```bash
   nmap -T1 <target>
   ```
   - يستخدم إعداد "T1" لجعل الفحص أبطأ وأكثر سرية.

### 22. **فحص دقيق باستخدام T0**
   ```bash
   nmap -T0 <target>
   ```
   - يجعل الفحص بطيئًا جدًا (Stealth Scan) لتجنب الحماية بشكل أكبر.

### 23. **فحص متعدد الأجهزة مع فاصل زمني**
   ```bash
   nmap -iL hosts.txt
   ```
   - يقرأ قائمة بالأهداف من ملف نصي ويقوم بفحصها واحداً تلو الآخر.

### 24. **تحديد خادم DNS مخصص**
   ```bash
   nmap --dns-servers <dns_server> <target>
   ```
   - يحدد خادم DNS معين بدلاً من الاعتماد على الإعداد الافتراضي.

### 25. **التخفي باستخدام فحص Maimon**
   ```bash
   nmap -sM <target>
   ```
   - يستخدم حزم Maimon للكشف عن المنافذ.

### 26. **فحص سريع للأجهزة المعروفة فقط**
   ```bash
   nmap -F <target>
   ```
   - يفحص فقط المنافذ الشائعة لسرعة أكبر.

### 27. **فحص بالبصمة الرقمية للهدف**
   ```bash
   nmap --data-length <num> <target>
   ```
   - يضيف حجم بيانات معين للحزم لمحاولة تجنب الاكتشاف.

### 28. **إعادة المحاولة لعدد مرات معين**
   ```bash
   nmap --max-retries <num> <target>
   ```
   - يحدد عدد إعادة المحاولات عند عدم استجابة المنافذ.

### 29. **كشف الأجهزة المتصلة بشبكة محلية (ARP Ping)**
   ```bash
   nmap -PR <target>
   ```
   - يستخدم ARP للكشف عن الأجهزة المتصلة على نفس الشبكة.

### 30. **فحص سريع للغاية (Aggressive Scan)**
   ```bash
   nmap -T5 <target>
   ```
   - يجعل الفحص أسرع ولكنه قد يزيد من فرص اكتشافه.

### 31. **تخطي المضيفين غير النشطين**
   ```bash
   nmap --host-timeout <time> <target>
   ```
   - يحدد وقتاً محدداً للتخلي عن فحص الأجهزة غير النشطة.

### 32. **فحص الأجهزة بدون حل DNS**
   ```bash
   nmap -n <target>
   ```
   - يتخطى تحليل DNS ويعمل على عناوين IP فقط.

### 33. **تحديد استجابة ICMP Echo**
   ```bash
   nmap -PE <target>
   ```
   - يرسل طلبات Echo Ping للكشف عن الأجهزة.

### 34. **إظهار معلومات إضافية أثناء الفحص**
   ```bash
   nmap -v <target>
   ```
   - يزيد من مستوى المعلومات المعروضة أثناء الفحص.

### 35. **زيادة مستوى التفاصيل في النتيجة**
   ```bash
   nmap -vv <target>
   ```
   - يعرض المزيد من المعلومات المفصلة.

### 36. **تحديد المنافذ باستخدام tcpflags**
   ```bash
   nmap --scanflags <flags> <target>
   ```
   - يحدد أعلام TCP مخصصة للفحص الخفي.

### 37. **تجاوز الكشف بتغيير توقيت الحزم**
   ```bash
   nmap --randomize-hosts <target>
   ```
   - يخلط ترتيب الأهداف ليصعب الكشف عن الفحص.

### 38. **تجاوز نظام IDS بفحص Fragmentation**
   ```bash
   nmap -f <target>
   ```
   - يكسر الحزم إلى أجزاء صغيرة لتجاوز IDS.

### 39. **فحص أجهزة خلف الجدران النارية**
   ```bash
   nmap -PN <target>
   ```
   - يتخطى فحص PING لفحص الأجهزة خلف الجدران النارية.

### 40. **تحديد واجهة شبكة معينة للفحص**
   ```bash
   nmap -e <interface> <target>
   ```
   - يحدد واجهة شبكة معينة مثل eth0 أو wlan0.

---

### 41-100: **أوامر متقدمة واستخدام السكربتات**




### فحص مخصص باستخدام سكربتات NSE

#### 41. **كشف الثغرات العامة**
   ```bash
   nmap --script vuln <target>
   ```
   - يكشف عن الثغرات الشائعة باستخدام مكتبة NSE الافتراضية.

#### 42. **تحليل الـSSL لاكتشاف مشكلات الأمان**
   ```bash
   nmap --script ssl-enum-ciphers <target>
   ```
   - يحلل الشهادات واكتشاف مشاكل SSL وTLS.

#### 43. **فحص HTTP واكتشاف بنية السيرفر**
   ```bash
   nmap --script http-headers <target>
   ```
   - يجمع رؤوس HTTP للهدف لتحليل الأمان.

#### 44. **اكتشاف كلمات المرور الضعيفة على FTP**
   ```bash
   nmap --script ftp-brute <target>
   ```
   - يحاول كشف كلمات المرور الضعيفة لخدمة FTP.

#### 45. **كشف خوادم DNS المفتوحة**
   ```bash
   nmap --script dns-open-resolver <target>
   ```
   - يكتشف ما إذا كان خادم DNS يسمح بالاستعلامات المفتوحة.

#### 46. **فحص مكتبات SMB لكشف الثغرات**
   ```bash
   nmap --script smb-vuln-ms17-010 <target>
   ```
   - يفحص خدمة SMB للتحقق من الثغرات المرتبطة بـ MS17-010.

#### 47. **تحليل البريد الإلكتروني لكشف SMTP**
   ```bash
   nmap --script smtp-commands <target>
   ```
   - يحلل أوامر SMTP لمعرفة أنواع الأوامر المدعومة.

#### 48. **فحص MySQL لاكتشاف الثغرات**
   ```bash
   nmap --script mysql-vuln-cve2012-2122 <target>
   ```
   - يكشف ثغرة CVE-2012-2122 في MySQL.

#### 49. **تحليل الأجهزة عبر خدمة SNMP**
   ```bash
   nmap --script snmp-info <target>
   ```
   - يجمع معلومات من الأجهزة التي تدعم SNMP.

#### 50. **فحص خدمة SSH وتحديد الإصدار**
   ```bash
   nmap --script ssh-hostkey <target>
   ```
   - يجمع مفاتيح التشفير لخدمة SSH.

---

### المزيد من أوامر تخصيص الفحص

#### 51. **زيادة مستوى التخفي باستخدام Time Decoy**
   ```bash
   nmap -D RND:10 <target>
   ```
   - يولد 10 عناوين IP عشوائية كطُعوم لإخفاء الفحص.

#### 52. **جمع معلومات DNS عن النطاق**
   ```bash
   nmap --script dns-brute <domain>
   ```
   - يقوم بكشف DNS على نطاق ويجمع السجلات.

#### 53. **فحص الأجهزة بناءً على Mac Address**
   ```bash
   nmap -A --script=mac-geoip <target>
   ```
   - يجمع الموقع الجغرافي للأجهزة باستخدام عنوان MAC.


### 54-100: **أوامر NSE إضافية حسب الخدمات والثغرات**

#### 54. **فحص نقاط الضعف المعروفة عبر بروتوكول HTTP**
   ```bash
   nmap --script http-vuln-cve2017-5638 <target>
   ```
   - يتحقق من ثغرة CVE-2017-5638 في الخوادم التي تستخدم Apache Struts.


### 55. **تحليل ملفات HTTP Robots**
   ```bash
   nmap --script http-robots.txt <target>
   ```
   - يفحص ملف `robots.txt` على الخوادم للكشف عن المسارات التي لا يرغب المسؤولون في فهرستها.

### 56. **فحص الثغرات المعروفة في WebDAV**
   ```bash
   nmap --script http-webdav-scan <target>
   ```
   - يفحص خدمة WebDAV للبحث عن ثغرات الوصول غير المصرح به.

### 57. **كشف DNS Zone Transfer**
   ```bash
   nmap --script dns-zone-transfer <domain>
   ```
   - يحاول نقل منطقة DNS لكشف معلومات الشبكة.

### 58. **فحص OpenSSH لكتابة رسائل التحذير**
   ```bash
   nmap --script ssh2-enum-algos <target>
   ```
   - يتحقق من خوارزميات SSH المدعومة في الخادم.

### 59. **اكتشاف خوادم NTP مفتوحة**
   ```bash
   nmap --script ntp-monlist <target>
   ```
   - يتحقق مما إذا كان خادم NTP يعرض قائمة بالأجهزة المتصلة.

### 60. **كشف كلمات المرور الافتراضية لـ HTTP**
   ```bash
   nmap --script http-default-accounts <target>
   ```
   - يكشف حسابات وكلمات مرور HTTP الافتراضية للأجهزة الشائعة.

### 61. **التأكد من وجود SSH Weak Ciphers**
   ```bash
   nmap --script ssh2-enum-ciphers <target>
   ```
   - يتحقق من خوارزميات التشفير الضعيفة المدعومة في SSH.

### 62. **فحص الـHTTP Methods المدعومة**
   ```bash
   nmap --script http-methods <target>
   ```
   - يكتشف أنواع HTTP المدعومة (GET، POST، DELETE، إلخ).

### 63. **تحليل بروتوكول الـSMTP لكشف Relay**
   ```bash
   nmap --script smtp-open-relay <target>
   ```
   - يتحقق إذا كان خادم SMTP يسمح بإعادة توجيه البريد غير المرغوب فيه.

### 64. **تحليل محتوى HTTP بدون جدار حماية**
   ```bash
   nmap --script http-waf-detect <target>
   ```
   - يتحقق مما إذا كان خادم HTTP محمي بجدار حماية للتطبيقات.

### 65. **تحليل الشبكات العشوائية عبر بروتوكول ICMP Echo**
   ```bash
   nmap -PE -iR <count>
   ```
   - يرسل طلبات ICMP إلى عدد عشوائي من الأجهزة (استطلاع عام).

### 66. **فحص أجهزة Windows عبر SMB Share**
   ```bash
   nmap --script smb-enum-shares <target>
   ```
   - يكشف عن المشاركات في نظام التشغيل Windows عبر بروتوكول SMB.

### 67. **تحديد المواقع الجغرافية للأجهزة باستخدام IP**
   ```bash
   nmap --script ip-geolocation-maxmind <target>
   ```
   - يستعين بقاعدة بيانات `MaxMind` لتحديد المواقع الجغرافية.

### 68. **فحص بروتوكول SIP للأجهزة**
   ```bash
   nmap --script sip-methods <target>
   ```
   - يكشف عن الطرق المدعومة في خوادم بروتوكول SIP.

### 69. **تحديد بروتوكول HTTP PUT للكشف عن الثغرات**
   ```bash
   nmap --script http-put <target>
   ```
   - يكتشف إمكانية رفع الملفات عبر HTTP PUT.

### 70. **فحص MySQL لاكتشاف بيانات الأنظمة**
   ```bash
   nmap --script mysql-info <target>
   ```
   - يكشف عن إصدارات وإعدادات MySQL المتوفرة.

### 71. **اختبار قواعد الجدران النارية باستخدام Fragment**
   ```bash
   nmap -f --mtu 24 <target>
   ```
   - يكسر الحزم للتغلب على بعض الجدران النارية المتشددة.

### 72. **تحليل خوادم DNS المتقدمة**
   ```bash
   nmap --script dns-service-discovery <target>
   ```
   - يستفسر عن خدمات DNS المتوفرة على الخادم.

### 73. **فحص النسخ الاحتياطي باستخدام TFTP**
   ```bash
   nmap --script tftp-enum <target>
   ```
   - يحاول استرداد بيانات الملفات المتاحة من خادم TFTP.

### 74. **تحليل خوادم HTTP وكشف إعدادات Cookie**
   ```bash
   nmap --script http-cookie-flags <target>
   ```
   - يحدد سياسة Cookie والأعلام الأمنية التي يستخدمها الخادم.

### 75. **تحليل خوادم الـDNS و كشف الإصدار**
   ```bash
   nmap --script dns-nsid <target>
   ```
   - يكتشف إصدار خادم DNS.

### 76. **اكتشاف VPN على TCP/UDP**
   ```bash
   nmap --script ike-version <target>
   ```
   - يتحقق من إعدادات IKE لبروتوكولات VPN.

### 77. **استخدام السكربتات لشن هجمات بروتوكول SMB**
   ```bash
   nmap --script smb-brute <target>
   ```
   - يجري هجمات القوة الغاشمة على مشاركة SMB.

### 78. **فحص بروتوكول NFS للكشف عن الأنظمة المشتركة**
   ```bash
   nmap --script nfs-showmount <target>
   ```
   - يكتشف المسارات المشتركة عبر NFS.

### 79. **جمع معلومات الـLDAP**
   ```bash
   nmap --script ldap-search <target>
   ```
   - يستعلم عن بيانات LDAP المتوفرة.

### 80. **تحديد البروتوكولات المدعومة لخدمات VPN**
   ```bash
   nmap --script ipsec-ike <target>
   ```
   - يكشف عن خوادم VPN التي تدعم بروتوكولات IPsec.

### 81. **كشف الأجهزة الخلفية في الـHTTP Proxy**
   ```bash
   nmap --script http-proxy-info <target>
   ```
   - يحدد الخوادم الخلفية في الشبكات التي تدعم الوكيل.

إليك الأوامر المتبقية لاستكمال الـ100:

---

### 82. **فحص الأجهزة عبر UPnP للكشف عن الخدمات**
   ```bash
   nmap --script upnp-info <target>
   ```
   - يكتشف معلومات الأجهزة والخدمات التي تدعم بروتوكول UPnP.

### 83. **فحص إصدار Apache للكشف عن الثغرات**
   ```bash
   nmap --script http-server-header <target>
   ```
   - يجمع معلومات حول إصدار Apache أو أي خادم ويب آخر للكشف عن نقاط الضعف.

### 84. **استخدام الـBanner Grabbing على Telnet**
   ```bash
   nmap --script telnet-encryption <target>
   ```
   - يجمع معلومات التشفير في خدمة Telnet، ويستخدم لتحليل التهيئات الضعيفة.

### 85. **فحص الثغرات الأمنية في MS SQL Server**
   ```bash
   nmap --script ms-sql-info <target>
   ```
   - يكشف عن إعدادات وثغرات قاعدة بيانات SQL Server.

### 86. **كشف إعدادات التشفير في IMAP**
   ```bash
   nmap --script imap-capabilities <target>
   ```
   - يفحص إعدادات التشفير والمزايا المدعومة لخدمة البريد IMAP.

### 87. **تحليل خادم HTTP لكشف دعم ضغط GZIP**
   ```bash
   nmap --script http-gzip <target>
   ```
   - يحدد ما إذا كان الخادم يدعم ضغط GZIP لتحسين الأداء.

### 88. **فحص الـRPC للكشف عن الخدمات المكشوفة**
   ```bash
   nmap -sR <target>
   ```
   - يفحص الخدمات التي تستخدم بروتوكول الـRPC ويحدد المنافذ المرتبطة بها.

### 89. **فحص بروتوكول NTP لاكتشاف إعدادات الوقت**
   ```bash
   nmap --script ntp-info <target>
   ```
   - يكشف إعدادات خادم NTP والوقت.

### 90. **تحليل المكونات الإضافية في بروتوكول SIP**
   ```bash
   nmap --script sip-enum-users <target>
   ```
   - يفحص مستخدمي SIP النشطين للكشف عن أسماء الحسابات.

### 91. **اختبار عناوين البريد الإلكتروني في SMTP**
   ```bash
   nmap --script smtp-enum-users <target>
   ```
   - يكشف عن أسماء مستخدمين عبر SMTP، مفيد لاختبار الحسابات النشطة.

### 92. **تحديد الموقع الجغرافي عبر قاعدة بيانات GeoLite**
   ```bash
   nmap --script ip-geolocation-geolite <target>
   ```
   - يستعين بقاعدة بيانات GeoLite للحصول على موقع الجهاز الجغرافي.

### 93. **فحص إعدادات X11 للكشف عن الوصول غير المصرح به**
   ```bash
   nmap --script x11-access <target>
   ```
   - يكشف عن الوصول غير المصرح به في إعدادات X11.

### 94. **فحص أداء بروتوكول الـSNMP للحصول على تفاصيل الشبكة**
   ```bash
   nmap --script snmp-netstat <target>
   ```
   - يستعرض بيانات الاتصالات النشطة في خوادم SNMP.

### 95. **تحليل بروتوكول الـSSH لتحديد خدمات الوكالة**
   ```bash
   nmap --script ssh-auth-methods <target>
   ```
   - يكشف أساليب المصادقة المدعومة في SSH.

### 96. **التعرف على خوادم Kerberos**
   ```bash
   nmap --script krb5-enum-users <target>
   ```
   - يكشف عن إعدادات خوادم Kerberos وأسماء المستخدمين.

### 97. **فحص بروتوكول RDP للكشف عن إعدادات سطح المكتب البعيد**
   ```bash
   nmap --script rdp-enum-encryption <target>
   ```
   - يتحقق من إعدادات التشفير والأمان في بروتوكول RDP.

### 98. **تحليل إعدادات HTTP Security Headers**
   ```bash
   nmap --script http-security-headers <target>
   ```
   - يكشف عن رؤوس الأمان التي يستخدمها الخادم لتحسين الأمان.

### 99. **التعرف على إعدادات الدعم في خدمة IRC**
   ```bash
   nmap --script irc-info <target>
   ```
   - يجمع معلومات حول إصدار خادم الـIRC والمزايا المدعومة.

### 100. **فحص إعدادات تبادل الملفات عبر Rsync**
   ```bash
   nmap --script rsync-list-modules <target>
   ```
   - يكشف عن إعدادات خدمة Rsync، ويحدد وحدات الملفات المشتركة التي يمكن الوصول إليها.


