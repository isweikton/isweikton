<div align="center">

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/header.svg" width="100%" alt="weikton — i take binaries apart and put them back as source" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=2800&pause=900&color=38BDF8&center=true&vCenter=true&width=880&height=46&lines=Reverse+engineering+GTA%3ASA+mobile%2C+byte+by+byte;C%2B%2B+%2F+ARM+Thumb-2+%2F+DWARF+archaeology;Android+native%3A+JNI%2C+NDK%2C+Kotlin%2C+Compose;SA%3AMP+internals%2C+RakNet%2C+Pawn;%2F%2F+TODO%3A" alt="what i do" />

<p>
  <a href="https://t.me/weikton_official"><img src="https://img.shields.io/badge/Telegram-111111?style=for-the-badge&logo=telegram&logoColor=2CA5E0" alt="Telegram" /></a>
  <a href="https://vk.com/weikton"><img src="https://img.shields.io/badge/VKontakte-111111?style=for-the-badge&logo=vk&logoColor=4F7DB3" alt="VKontakte" /></a>
  <a href="https://github.com/isweikton?tab=repositories"><img src="https://img.shields.io/badge/35%20repos-111111?style=for-the-badge&logo=github&logoColor=E6EDF3" alt="repositories" /></a>
  <a href="https://github.com/isweikton?tab=followers"><img src="https://img.shields.io/github/followers/isweikton?style=for-the-badge&label=followers&labelColor=111111&color=111111&logo=github&logoColor=38BDF8" alt="followers" /></a>
</p>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<h3><code>&nbsp;// whoami&nbsp;</code></h3>

</div>

```console
$ nm -C libweikton.so --defined-only

0x00000010 T weikton::reverse(libGame.so&)        // gta:sa 2.10 — arm & arm64, no guessing
0x00000024 T weikton::cpp::rewrite(Binary&)       // 1:1 with the original, hooks are cheating
0x00000038 T weikton::android::native(JNIEnv*)    // jni, ndk, .so surgery, 16 KB pages
0x0000004c T weikton::pawn::amx(cell* script)     // sa:mp internals, raknet, packets
0x00000060 T weikton::kotlin::compose(Ui&&)       // when the thing needs a face
0x00000074 T weikton::design::figma(Pixel* px)    // ui/ux, layout, pixel discipline
0x0000ffff T weikton::sleep()                     // never called
```

<div align="center">

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<h3><code>&nbsp;// how a binary becomes source&nbsp;</code></h3>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/pipeline.svg" width="92%" alt="libGame.so to DWARF to disassembly to c++ to engine" />

<sub>no hooks · no hardcoded addresses · the disassembler is always right</sub>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<h3><code>&nbsp;// stack&nbsp;</code></h3>

<p>
  <img src="https://img.shields.io/badge/C%2B%2B-111111?style=for-the-badge&logo=cplusplus&logoColor=00599C" />
  <img src="https://img.shields.io/badge/C-111111?style=for-the-badge&logo=c&logoColor=A8B9CC" />
  <img src="https://img.shields.io/badge/ARM%20%2F%20ARM64-111111?style=for-the-badge&logo=arm&logoColor=0091BD" />
  <img src="https://img.shields.io/badge/Reverse%20Engineering-111111?style=for-the-badge&logo=hackaday&logoColor=E6EDF3" />
  <img src="https://img.shields.io/badge/CMake-111111?style=for-the-badge&logo=cmake&logoColor=DA3434" />
  <img src="https://img.shields.io/badge/Pawn-111111?style=for-the-badge&logo=quicklook&logoColor=94A3B8" />
</p>

<p>
  <img src="https://img.shields.io/badge/Android-111111?style=for-the-badge&logo=android&logoColor=3DDC84" />
  <img src="https://img.shields.io/badge/NDK%20%2F%20JNI-111111?style=for-the-badge&logo=android&logoColor=3DDC84" />
  <img src="https://img.shields.io/badge/Kotlin-111111?style=for-the-badge&logo=kotlin&logoColor=7F52FF" />
  <img src="https://img.shields.io/badge/Java-111111?style=for-the-badge&logo=openjdk&logoColor=ED8B00" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-111111?style=for-the-badge&logo=jetpackcompose&logoColor=4285F4" />
  <img src="https://img.shields.io/badge/Gradle-111111?style=for-the-badge&logo=gradle&logoColor=02303A" />
</p>

<p>
  <img src="https://img.shields.io/badge/GTA%3ASA-111111?style=for-the-badge&logo=rockstargames&logoColor=FCAF17" />
  <img src="https://img.shields.io/badge/SA%3AMP-111111?style=for-the-badge&logo=gamejolt&logoColor=FACC15" />
  <img src="https://img.shields.io/badge/RenderWare-111111?style=for-the-badge&logo=unrealengine&logoColor=94A3B8" />
  <img src="https://img.shields.io/badge/Figma-111111?style=for-the-badge&logo=figma&logoColor=F24E1E" />
  <img src="https://img.shields.io/badge/UI%2FUX-111111?style=for-the-badge&logo=materialdesign&logoColor=22C55E" />
  <img src="https://img.shields.io/badge/Layout-111111?style=for-the-badge&logo=html5&logoColor=E34F26" />
</p>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<h3><code>&nbsp;// selected work&nbsp;</code></h3>

<table>
<tr>
  <td><a href="https://github.com/isweikton/WNPatcher"><b>WNPatcher</b></a></td>
  <td>ARM &amp; ARM64 patch library for GTA:SA and SA:MP Mobile</td>
  <td><img src="https://img.shields.io/github/stars/isweikton/WNPatcher?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
<tr>
  <td><a href="https://github.com/isweikton/gtasa-android-sourcecode"><b>gtasa-android-sourcecode</b></a></td>
  <td>Recovered source layout of GTA:SA Android</td>
  <td><img src="https://img.shields.io/github/stars/isweikton/gtasa-android-sourcecode?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
<tr>
  <td><a href="https://github.com/isweikton/RPCReciever-Plugin-SAMPMobile"><b>RPCReciever</b></a></td>
  <td>Sending and intercepting SA:MP RPC packets on mobile</td>
  <td><img src="https://img.shields.io/github/stars/isweikton/RPCReciever-Plugin-SAMPMobile?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
<tr>
  <td><a href="https://github.com/isweikton/ingame-recording-system-sampandroid"><b>ingame-recording-system</b></a></td>
  <td>In-game recording built into a SA:MP Android client</td>
  <td><img src="https://img.shields.io/github/stars/isweikton/ingame-recording-system-sampandroid?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
<tr>
  <td><a href="https://github.com/isweikton/pawn-android"><b>pawn-android</b></a></td>
  <td>Pawn 3.2.3664 ported to Android, 16 KB pages, both ABIs</td>
  <td><img src="https://img.shields.io/github/stars/isweikton/pawn-android?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
<tr>
  <td><a href="https://github.com/isweikton/samp-android-cef"><b>samp-android-cef</b></a></td>
  <td>Chromium Embedded inside SA:MP mobile — <i>it&apos;s a dream?</i></td>
  <td><img src="https://img.shields.io/github/stars/isweikton/samp-android-cef?style=flat-square&labelColor=111111&color=38BDF8&logo=github&logoColor=E6EDF3&label=" alt="" /></td>
</tr>
</table>

<sub>plus dumps, model lists, hud patches, textdraw tooling — <a href="https://github.com/isweikton?tab=repositories">all 35 repositories</a></sub>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<h3><code>&nbsp;// telemetry&nbsp;</code></h3>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=isweikton&theme=github_dark" width="92%" alt="profile summary" />

<p>
  <img height="185" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=isweikton&theme=github_dark" alt="repos per language" />
  <img height="185" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=isweikton&theme=github_dark" alt="most commit language" />
</p>

<p>
  <img height="185" src="https://streak-stats.demolab.com?user=isweikton&hide_border=true&background=0D1117&stroke=1B2530&border=1B2530&ring=38BDF8&fire=38BDF8&currStreakLabel=38BDF8&sideLabels=94A3B8&dates=475569&currStreakNum=E6EDF3&sideNums=E6EDF3" alt="streak" />
  <img height="185" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=isweikton&theme=github_dark&utcOffset=3" alt="productive time" />
</p>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=isweikton&bg_color=0D1117&color=E6EDF3&line=38BDF8&point=7DD3FC&area=true&area_color=0EA5E9&hide_border=true&custom_title=commits%20over%20time" width="92%" alt="activity" />

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/divider.svg" width="90%" alt="" />

<p>
  <a href="https://count.getloli.com" target="_blank">
    <img alt="Moe Counter!" src="https://count.getloli.com/@isweikton.github?name=isweikton.github&theme=booru-jaypee&padding=7&offset=0&align=top&scale=1&pixelated=0&darkmode=auto" />
  </a>
</p>

<img src="https://raw.githubusercontent.com/isweikton/isweikton/main/assets/footer.svg" width="100%" alt="weikton — c++ / reverse engineering / android" />

</div>
