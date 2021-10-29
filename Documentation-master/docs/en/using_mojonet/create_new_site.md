# Create new mojonet site

## Easy way: Using the web interface

- Click on **⋮** > **"Create new, empty site"** menu item on the site [mojoHello].
- You will be **redirected** to a completely new site that is only modifiable by you!
- You can find and modify your site's content in **data/[yoursiteaddress]** directory
- After the modifications open your site, drag the topright "0" button to left, then press **sign** and **publish** buttons on the bottom

## Manual way: Using the command line

> **Note:**
> If you are using pre-boundled mojonet distribution, then in place of `mojonet.py` you need to use `./mojonet.sh` (Linux), `lib/mojonet.cmd` (Windows), `mojonet.app/Contents/MacOS/mojonet` (macOS)

### 1. Create site structure

- Shut down mojonet if it is running
- Browse to the folder where mojonet is installed and run:

```bash
$ mojonet.py siteCreate
...
- Site private key: 23DKQpzxhbVBrAtvLEc2uvk7DZweh4qL3fn3jpM3LgHDczMK2TtYUq
- Site address: 13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2
...
- Site created!
$ mojonet.py
...
```

- This will create the initial files for your site inside `data/13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2`.

### 2. Build/Modify site

- Update the site files located in `data/[your site address key]` (eg: 13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2).
- When your site is ready run:

```bash
$ mojonet.py siteSign 13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2
- Signing site: 13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2...
Private key (input hidden):
```

- Enter the private key you got when you created the site. This will sign all files so peers can verify that the site owner is who made the changes.

### 3. Publish site changes

- In order to inform peers about the changes you made you need to run:

```bash
$ mojonet.py sitePublish 13DNDkMUExRf9Xa9ogwPKqp7zyHFEqbhC2
...
Site:13DNDk..bhC2 Publishing to 3/10 peers...
Site:13DNDk..bhC2 Successfuly published to 3 peers
- Serving files....
```

- That's it! You've successfully signed and published your modifications.
- Your site will be accessible 

**Next steps:** [mojonet Developer Documentation](../../site_development/getting_started/)
