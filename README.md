To Do:

- [ ] Updates FAQ

- [ ] Upated Install instructions

- [ ] Update Resume Tips & tricks

- [ ] Get screenshots of app 

- [ ] InternBot applies only to internships

- [ ] Code obfuscation – to ensure that no one can reverse engineer the application.
      To obfuscate your application, multiple tools can be used. 
      You can either use packages such as pyarmor that are made to obfuscate Python code or open source tools such as pyinstaller in combination with cpython (for most       sensitive code).

- [ ] License verification – to ensure that customers need a license key before they can use the application 
      (eg. so that you can restrict which features they can use and how long the license is valid).
      icense verification

A license key can be easily verified using the code below. You can find more information about the parameters here.

'python
from licensing.helpers import Helpers
from licensing.models import Response, RSAPublicKey
from licensing.methods import Key

pubKey = "<RSAKeyValue><Modulus>sGbvxwdlDbqFXOMlVUnAF5ew0t0WpPW7rFpI5jHQOFkht/326dvh7t74RYeMpjy357NljouhpTLA3a6idnn4j6c3jmPWBkjZndGsPL4Bqm+fwE48nKpGPjkj4q/yzT4tHXBTyvaBjA8bVoCTnu+LiC4XEaLZRThGzIn5KQXKCigg6tQRy0GXE13XYFVz/x1mjFbT9/7dS8p85n8BuwlY5JvuBIQkKhuCNFfrUxBWyu87CFnXWjIupCD2VO/GbxaCvzrRjLZjAngLCMtZbYBALksqGPgTUN7ZM24XbPWyLtKPaXF2i4XRR9u6eTj5BfnLbKAU5PIVfjIS+vNYYogteQ==</Modulus><Exponent>AQAB</Exponent></RSAKeyValue>"

res = Key.activate(token="WyIyNTU1IiwiRjdZZTB4RmtuTVcrQlNqcSszbmFMMHB3aWFJTlBsWW1Mbm9raVFyRyJd",\
                   rsa_pub_key=pubKey,\
                   product_id=3349, key="ICVLD-VVSZR-ZTICT-YKGXL", machine_code="test")

if res[0] == None:
    print("An error occured: {0}".format(res[1]))
else:
    print("Success")
'

- [ ] Webshop – so that customers can obtain a license key to unlock functionality. When you have obfuscation and license verification in place, we need a way for customers to be able to order a license key. If you already have Stripe, you can use the recurring billing module, which acts like an interface for plans defined in your Stripe account. 
-----
https://www.youtube.com/watch?v=jp0eiGn4jto

https://github.com/harshibar/common-intern/blob/master/README.md

https://github.com/ameeno/LinkedIn-Bot-1/blob/master/configure.py

https://github.com/harshibar/common-intern/tree/7947ed6f151e5b9b1792c4bc7a7623212fa3f8bc

https://www.youtube.com/watch?v=N_7d8vg_TQA&feature=youtu.be

https://github.com/harshibar/5-python-projects

https://github.com/harshibar/common-intern

https://cryptolens.io/2019/11/tips-on-monetizing-python-applications/
