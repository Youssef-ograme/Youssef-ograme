<img width="300" height="88" alt="inzo_readme" src="https://github.com/user-attachments/assets/e813e924-7843-4bcd-b49e-942db9ccbaeb" />
<svg width="100%" viewBox="0 0 680 200" xmlns="http://www.w3.org/2000/svg">
  <rect width="680" height="200" fill="#0a0a0a" rx="12"/>

  <!-- scanline -->
  <rect width="680" height="40" fill="#1D9E75" opacity="0.04" rx="0">
    <animateTransform attributeName="transform" type="translate" from="0,-40" to="0,200" dur="3s" repeatCount="indefinite"/>
  </rect>

  <!-- INZO glitch text -->
  <text x="340" y="80" text-anchor="middle" font-family="monospace" font-size="52" font-weight="500" fill="#1D9E75" letter-spacing="10">
    INZO
    <animate attributeName="opacity" values="1;1;0.8;1;1;0.6;1" dur="4s" repeatCount="indefinite"/>
  </text>
  <!-- glitch red -->
  <text x="344" y="80" text-anchor="middle" font-family="monospace" font-size="52" font-weight="500" fill="#E24B4A" letter-spacing="10" opacity="0">
    INZO
    <animate attributeName="opacity" values="0;0;0.6;0;0;0.4;0" dur="4s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,0;-4,0;4,0;0,0" dur="4s" repeatCount="indefinite"/>
  </text>
  <!-- glitch blue -->
  <text x="336" y="80" text-anchor="middle" font-family="monospace" font-size="52" font-weight="500" fill="#378ADD" letter-spacing="10" opacity="0">
    INZO
    <animate attributeName="opacity" values="0;0;0.5;0;0;0.3;0" dur="4s" begin="0.05s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,0;4,0;-4,0;0,0" dur="4s" repeatCount="indefinite"/>
  </text>

  <!-- subtitle -->
  <text x="340" y="110" text-anchor="middle" font-family="monospace" font-size="12" fill="#5DCAA5" letter-spacing="4">
    STUDENT @ 1337 — 42 NETWORK
    <animate attributeName="opacity" values="0;0;1" dur="2s" fill="freeze"/>
  </text>

  <!-- loading bar bg -->
  <rect x="140" y="135" width="400" height="6" rx="3" fill="#111" stroke="#1D9E75" stroke-width="0.5">
    <animate attributeName="opacity" values="0;0;1" dur="2.5s" fill="freeze"/>
  </rect>
  <!-- loading bar fill -->
  <rect x="140" y="135" width="0" height="6" rx="3" fill="#1D9E75">
    <animate attributeName="opacity" values="0;0;1" dur="2.5s" fill="freeze"/>
    <animate attributeName="width" values="0;400" dur="2s" begin="1s" fill="freeze"/>
  </rect>

  <!-- icons -->
  <!-- C -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" x="120" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3s" fill="freeze"/>
  </image>
  <!-- C++ -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" x="170" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.15s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.15s" fill="freeze"/>
  </image>
  <!-- Python -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" x="220" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.3s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.3s" fill="freeze"/>
  </image>
  <!-- Bash -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" x="270" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.45s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.45s" fill="freeze"/>
  </image>
  <!-- Linux -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" x="320" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.6s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.6s" fill="freeze"/>
  </image>
  <!-- Git -->
  <image href="" x="370" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.75s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.75s" fill="freeze"/>
  </image>
  <!-- Vim -->
  <image href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vim/vim-original.svg" x="420" y="158" width="36" height="36" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.9s" fill="freeze"/>
    <animateTransform attributeName="transform" type="translate" values="0,15;0,0" dur="0.4s" begin="3.9s" fill="freeze"/>
  </image>

  <!-- [ coding in progress... ] -->
  <text x="340" y="195" text-anchor="middle" font-family="monospace" font-size="10" fill="#1D9E75" letter-spacing="2" opacity="0">
    [ CODING IN PROGRESS... ]
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="4.2s" fill="freeze"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="2s" begin="4.7s" repeatCount="indefinite"/>
  </text>
</svg>
