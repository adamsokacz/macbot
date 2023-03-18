---
description: Establishing a remote desktop connection to the MacBot unit
---

# Connect

## Install MobaXTerm

{% embed url="https://mobaxterm.mobatek.net/download-home-edition.html" %}
If on a lab PC, choose 'Portable', otherwise choose 'Installer'
{% endembed %}

## Connection Profiles

### Profile Links

{% embed url="https://raw.githubusercontent.com/adamsokacz/macbot/main/docs/Labs/Profiles/MacBot_SSH.moba" %}
SSH Bash Profile
{% endembed %}

{% embed url="https://raw.githubusercontent.com/adamsokacz/macbot/main/docs/Labs/Profiles/MacBot_VNC.moba" %}
VNC Profile
{% endembed %}

### Save each profile using the following steps:

* Click profile RAW link
* Click **Save Page As**

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

* Change file type to **All Files**

<figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* Save to your Desktop/

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

## Lab Network

Use the following credentials to connect to the lab network on your personal PC:

{% content-ref url="page-1.md" %}
[page-1.md](page-1.md)
{% endcontent-ref %}

## Connecting

Click the MacBot\_SSH profile . MobaXTerm will open.

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Search for a **MacBot##** label on your MacBot unit

![](<.gitbook/assets/image (8).png>)

Create an **SSH tunnel** to your MacBot unit over the **lab network.**

{% tabs %}
{% tab title="Bash Command" %}
```bash
ssh -L 5902:localhost:5902 jnano@macbot01
```
{% endtab %}

{% tab title="Template" %}
```bash
ssh -L PC_Port:localhost:MacBot_Port user@pc_ip_or_name##
```


{% endtab %}
{% endtabs %}

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Start the VNC server by using **\~./autostart\_vnc.bash**

```bash
~/autostart_vnc.bash
```

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Without closing the SSH tunnel tab, load the VNC profile

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Enter the provided **MacBot password**:

{% content-ref url="page-1.md" %}
[page-1.md](page-1.md)
{% endcontent-ref %}

A VNC session will be established

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Click **Fullscreen** and untoggle **Always on Top**.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

You can now use **TAB + Windows** to toggle between your open tabs

<figure><img src=".gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>
