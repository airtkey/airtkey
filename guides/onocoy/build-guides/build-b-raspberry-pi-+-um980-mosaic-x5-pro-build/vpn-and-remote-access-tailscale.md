---
layout:
  width: default
  title:
    visible: false
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# VPN & Remote Access (Tailscale)

## VPN & Remote Access (Tailscale)

Tailscale creates a secure, peer-to-peer VPN that lets you access your base station from anywhere in the world — without complex firewall configuration or port forwarding.

***

### 🤔 Why Use Tailscale?

| Traditional Port Forwarding       | Tailscale                       |
| --------------------------------- | ------------------------------- |
| Need to configure firewall/router | Works out-of-the-box            |
| May not work behind NAT           | Works through any NAT           |
| Security risks with open ports    | Encrypted, authenticated access |
| Limited to local network          | Access from anywhere            |

***

### ✅ ELT\_RTKBase — Built-in Tailscale Support

> 💡 **Good news:** ELT\_RTKBase already includes Tailscale — no manual installation required!

#### Steps:

**1. Open the ELT\_RTKBase Web Interface**

Go to your dashboard in the browser:\
rtkbase.local

**2. Navigate to Settings → VPN**

Scroll down to the bottom of the Settings page.\
You will find the **VPN** section with the button:

> **Tailscale Admin Console**

**3. Click the Button**

> ⚠️ **Note:** The Tailscale admin console opens as a **pop-up window**.\
> Some browsers (especially Chrome) may block this pop-up.\
> If nothing happens, check your browser's address bar for a blocked pop-up notification and allow it.

**4. Log In to Tailscale**

* Create a free account at [tailscale.com](https://tailscale.com/) if you don't have one yet
* Log in with your account (email, Google, or GitHub)
* Authorize the device

**5. Done — You're Connected!**

Once authenticated, ELT\_RTKBase will automatically connect to your Tailscale network.\
You can now access your dashboard remotely from anywhere using your **Tailscale IP** (`100.x.x.x`).

***

### 📱 Access from Mobile Devices

1. Install the **Tailscale app** from the [App Store](https://apps.apple.com/) / [Play Store](https://play.google.com/)
2. Log in with the **same Tailscale account**
3. Your Raspberry Pi will appear in the device list
4. Open your browser and go to `http://100.x.x.x`

***

### 🛠️ Tailscale Commands Reference

> ℹ️ These commands are only needed if you manage Tailscale manually via SSH.\
> For most users, the built-in ELT\_RTKBase integration is sufficient.

| Command               | Description            |
| --------------------- | ---------------------- |
| `sudo tailscale up`   | Connect / authenticate |
| `sudo tailscale down` | Disconnect VPN         |
| `tailscale status`    | Show connected devices |
| `tailscale ip -4`     | Show Tailscale IPv4    |
| `tailscale logout`    | Log out from Tailscale |

***

### 🐛 Troubleshooting

**Pop-up blocked by browser**

* Look for a pop-up blocked icon in your browser's address bar
* Click it and select **"Always allow pop-ups from this site"**
* Try again

**Can't reach dashboard remotely**

```bash
# Check Tailscale status via SSH
sudo tailscale status

# Restart Tailscale
sudo systemctl restart tailscaled

# Need to re-authenticate
sudo tailscale logout
sudo tailscale up
```

***

## 📂 Related Documentation

* [ELT\_RTKBase Documentation](https://github.com/GNSSOEM/ELT_RTKBase)
* [Tailscale Documentation](https://tailscale.com/kb/)
