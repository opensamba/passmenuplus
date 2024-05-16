passmenu-otp
============

A simple extension of [passmenu][passmenu] friendly to Wayland desktop and 
supporting pass otp extention often used in two-factor authentication (2FA).


## What is this?

[pass](https://www.passwordstore.org/) is a minimalistic password manager, which became known thanks to
its incredible versatility and abundance of extension points.

One tool which makes _pass_ extremely convenient for everyday use is
[passmenu](https://git.zx2c4.com/password-store/tree/contrib/dmenu) -- a shell script, which utilizes _dmenu_ to offer user
interactive list of available passwords. Having selected a specific password,
user can copy it to clipboard temporarily, or use any tool to input it into
focused text area.

Among others, _pass_ can also be used to manage one-time passwords (OTP),
commonly used for two-factor authentication (2FA). This is done using
[pass-otp][pass-otp]. Sadly, since the command-line invocation differs for OTP's
and conventional passwords, _passmenu_ cannot be used with OTP's out of the box,
forcing users to clumsily open a new shell everytime they need to generate a OTP.
This not only creates time strain on the user's productivity, but also raises
overall stress levels since OTP use is often limited to couple of seconds only.

This project attempts to very simply resolve this problem by bringing support
for OTP's to your friendly neighborhood _passmenu_.


## How to use it?

_passmenu-otp_ works the same way as _passmenu_:

  1. Run it (from shell or using keybinding).
  2. Pick a password in passmenu.
  3. The password gets copied to your X clipboard for a limited amount of time.

The **additional feature** is if you select password with content `otpauth://`, the script
automatically uses *pass otp* to generate an OTP, and **copies that number** to your clipboard instead!


## Security Considerations

If you don't trust your device or your environment, don't use this tool.


## Copyright

This mod was created in April 2019 by Petr Mánek, and is licensed under the MIT
license. For copyright of the original work, check out [its repository][passmenu].


[pass]: https://github.com/peff/pass
[passmenu]: https://github.com/cdown/passmenu
[pass-otp]: https://github.com/tadfisher/pass-otp

