# ❓ FAQ & Troubleshooting

### 🔧 General

**Q: My GNSS receiver is not detected after installation.**

> Make sure you connected the GNSS receiver **and the antenna** BEFORE running the installation script.\
> Reconnect the device and restart the service via the ELT\_RTKBase dashboard.

***

**Q: The installation finished with an error message — is that normal?**

> Yes, in most cases this can be ignored.\
> Simply open your browser and check if the dashboard is accessible at `http://rtkbase.local`.

***

**Q: The dashboard is not loading in my browser.**

> * Make sure your PC/phone is on the **same network** as the Raspberry Pi
> * Try using the IP address directly instead of `rtkbase.local`
> * Check that the Raspberry Pi is powered on and connected to your router

***

**Q: I forgot my login credentials for the dashboard.**

> The default credentials are set during the ELT\_RTKBase installation.\
> Check the [ELT\_RTKBase Documentation](https://github.com/GNSSOEM/ELT_RTKBase/blob/main/Doc/ELT_RTKBase_v1.8.1_EN.pdf) for password reset instructions.

***

### 📡 GNSS & Signal

**Q: I have no satellites / signal fix.**

> * Make sure the antenna is connected and has a **clear view of the sky**
> * Indoor use is not recommended — place the antenna outside or near a window
> * Wait a few minutes after startup for the receiver to acquire satellites

***

**Q: My signal quality is poor.**

> * Check the antenna cable for damage
> * Avoid placing the antenna near metal surfaces or under obstacles
> * Use a ground plane if required for your antenna type

***

### 🌐 Connectivity & Remote Access

**Q: The Tailscale pop-up is being blocked by my browser.**

> Chrome and other browsers may block pop-ups by default.\
> Look for the blocked pop-up icon in your browser's address bar, click it and select **"Always allow pop-ups from this site"**.

***

**Q: I can't reach my dashboard remotely via Tailscale.**

> * Make sure Tailscale is connected on both devices
> * Use the Tailscale IP (`100.x.x.x`) in your browser
> * Check Tailscale status via SSH:
>
> ```bash
> sudo tailscale status
> ```

***

**Q: SSH connection is not working.**

> * Make sure SSH was enabled in the **Raspberry Pi Imager** before flashing
> * Check that you are using the correct IP address
> * Try restarting the Raspberry Pi

***

### 🛰️ onocoy / Network Integration

**Q: My station is not showing up on onocoy.**

> * Double check your onocoy credentials in the ELT\_RTKBase settings
> * Make sure your internet connection is stable
> * Check the onocoy status page for any service outages
