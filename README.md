[![sd_partition_erista_oled](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/blue_aio_wall_banner.png)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)



---

<div align="center">

![GitHub License](https://img.shields.io/github/license/Atmosphere-NX/Atmosphere?style=for-the-badge&labelColor=123ede&color=123ede)&emsp;&emsp;
[![NX blue pack - AIO CFW PACK](https://img.shields.io/github/v/release/glitched-nx/blue_pack_nx?style=for-the-badge&label=NX%20blue%20pack%20-%20AIO%20CFW%20PACK&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)&emsp;&emsp;
[![NX blue pack DLs](https://img.shields.io/github/downloads/glitched-nx/blue_pack_nx/total?style=for-the-badge&label=NX%20blue%20pack%20Downloads&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)

<div align="center" style="font-size: 2em;">
  <img src="https://img.shields.io/github/v/release/THZoria/NX_Firmware?style=for-the-badge&label=Aktuelle%20Systemversion&labelColor=123ede&color=b3b9e8" alt="Aktuelle Systemversion" />&emsp;
  <img src="https://img.shields.io/github/v/release/glitched-nx/atmosphere_blue?include_prereleases&style=for-the-badge&label=ATMO BLUE&labelColor=123ede&color=b3b9e8" alt="ATMO BLUE" />
  </p>
</div>

---

<div align="center">

[![CFW - Homebrew - Modding Deutschland](https://img.shields.io/badge/CFW%20--%20Homebrew%20--%20Modding%20Deutschland-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://facebook.com/groups/switchcfwde)&emsp;&emsp;
[![NX blue pack WIKI](https://img.shields.io/badge/NX%20blue%20pack%20WIKI-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://github.com/glitched-nx/blue_pack_NX/wiki)

</div>

---



<h2 style="font-family: Arial, sans-serif; font-size: 24px;">
  <a href="https://github.com/glitched-nx/blue_pack_NX/releases/latest" style="text-decoration: none; color: #ffffff;">
    NX blue pack
  </a>
  <span id="version" style="color: #ff0000; font-weight: normal;"></span>
</h2>

<script>
  fetch("https://api.github.com/repos/glitched-nx/blue_pack_NX/releases/latest")
    .then(response => response.json())
    .then(data => {
      // Entferne das "v" falls vorhanden
      const version = data.tag_name.startsWith("v") ? data.tag_name.slice(1) : data.tag_name;
      document.getElementById("version").textContent = version;
    })
    .catch(error => console.error("Error fetching version:", error));
</script>

