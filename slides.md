---
# try also 'default' to start simple
theme: default
# apply any windi css classes to the current slide
class: "text-center bg-light-secondary-container text-light-on-secondary-container"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false

fonts:
  sans: "Montserrat"
  serif: "Robot Slab"
  mono: "Inconsolata"
---

# Frame Relay

## Group 14

<Counter />

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
class: "bg-light-surface text-light-on-surface"
---

# Team members

- Duong Tien Vinh - 19127631
- Nguyen Le Huu Sang - 19127538

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

---

# Table of Contents:

- Definition
- How does frame relay work
- Types of Frame Relay Connections
- Benefit of using frame Relay

---

# Definition:

Frame Relay is a standardized wide area network technology that specifies the physical and data link layers of digital telecommunications channels using packet switching. Originally designed to transport over Integrated Services Digital Network (ISDN) infrastructure, it can today be used in the context of many other network interfaces.

<img
  src="/frame-relay.png"
  class="h-1/2 w-1/2"
/>

---

# Definition:
The Frame Relay network handles transmission over a constantly changing path
that is transparent to all widely used end-user WAN protocols. It is less
expensive than rental lines and that is one reason for its popularity. The
extreme simplicity of configuring user devices in a Frame Relay network provides
another reason for the popularity of Frame Relay.

- Due to the development of technology, Frame Relay were gradually replaced by
  Multiprotocol Label Switching (MPLS). MPLS allows for a blending of frame
  relay, ATM, ethernet, and Internet Protocol (IP) networks into a single
  infrastructure. This has helped companies integrate their telecommunications
  in one system that could transmit all sorts of data, including voice and video
  data transfer.
- However, many rural areas still lack DSL and cable modem services. In such
  cases, the least expensive non-dial connection type is still the 64 kbit/s
  Frame Relay line. Thus, a retail chain, for example, could use Frame Relay to
  connect rural stores to their corporate LAN.


---

# How does frame relay work:

Frame relay uses packet switching technology. This means that it breaks data,
such as call data, into smaller packets, also known as frames, to transmit it
through a shared frame relay network. Frame relay is based on older X.25
packet-switching technology that was designed for sending analog data such as
voice conversations. But, unlike X.25, frame relay is a fast packet technology.
That means the protocol does not attempt to correct errors. When an error is
detected in a frame, it is simply dropped. The endpoints are responsible for
detecting and retransmitting dropped frames. The error incidence in digital
networks is small relative to analog networks. These data packets are then
reassembled at the data’s destination. Frame relay has long been used as part of
many companies’ Integrated Services Digital Network (ISDN) systems. It’s often
considered to be the streamlined update to the older type of packet switching
tech.

<img
  src="/osi-model.png"
  class="h-1/5 w-1/5"
/>

---

# How does frame relay work:

This process may also be explained in terms of data equipment, specifically data
communications equipment (DCE) and data terminal equipment (DTE). For a frame
relay WAN to send data, DTE and DCE (data circuit-terminating equipment –
another name of DCE) are required. In frame relay services, the DCE is the frame
relay switch, as this provides the service, and the DTE is your routers, the
devices that receive the service.

<img
  src="/mesh.png"
  class="h-1/2 w-1/2"
/>

Frame relay uses the first two layers of the OSI model, a physical layer and a
data link layer, which also make up the first layer of the TCP/IP model; the
network interface layer.

---

# Types of Frame Relay Connections


Switched Virtual Circuits
- SVCs are essentially short-term virtual circuits. They are used when data
  needs to be transmitted across a virtual circuit and then that virtual circuit
  can be closed again.

- A typical example of an SVC is when a user downloads a file. The SVC is
  created, connects the user and the file download server, and then when the
  download is complete the connection is immediately terminated.

Permanent Virtual Circuits
- PVCs are, unlike SVCs, permanent. PVCs are a permanent connection between
  nodes in a frame relay network or an asynchronous transfer mode (ATM) network.

- They are the more common type of frame relay connection as they are used by
  companies who need a permanent connection with multiple routers, such as a
  company that regularly makes long-distance calls between two of its offices.

---

# Benefit of using frame Relay:

- Efficient. It does not perform error correction, which consumes time and
  network resources. Its use of use variable packet sizes improves bandwidth
  use.
- Cost-effective. It's cheaper than dedicated lines and less hardware is required.
- Flexible. It uses a data link connection identifier (DLCI) number. The DLCI is
  a number that identifies the logical circuit between the router and the frame
  relay switch. It determines which circuit to send a frame to in a frame relay
  network, allowing any two stations to connect. Frame relay flexibility also
  comes from its ability to buffer traffic bursts.
- Low latency. It's less prone to latency because other network components handle error correction.
- Higher Data Rates: In comparison to dedicated lines, frame relays are much
  cheaper for companies that need to maintain connections between multiple
  routers across a WAN. This is because the company is not paying for the full
  bandwidth of each access line as they would for leased lines. Instead, the
  cost of the bandwidth is shared by everyone using it.

---

# Benefit of using frame Relay:

- Can Handle Data in Bursts: One of the reasons frame relay is often preferred
  to leased lines is because companies are not constantly transmitting data.
  This means that the bandwidth of leased lines is rarely being used in full,
  especially if lines are required to lesser-used routers. Frame relay resolves
  this problem by using busty technology and shared bandwidth, set by the CIR.
- Lower Overheads: In comparison to dedicated lines, frame relays are much
  cheaper for companies that need to maintain connections between multiple
  routers across a WAN. This is because the company is not paying for the full
  bandwidth of each access line as they would for leased lines. Instead, the
  cost of the bandwidth is shared by everyone using it.

---

# Benefit of using frame Relay:

- Local Management Interface (LMI) Enhancements: Since the inception of frame
  relay, enhancements have been developed to improve frame relay services and
  their functionality in complex networks. Ex of LMI developed include.
    - A keepalive mechanism, which verifies data flow and provides flow control.
    - A status mechanism, which creates real-time status reports on the DLCIs known to the switch.
    - LMI multicasting extensions, which save bandwidth by allowing routing
      updates and messages that alert user devices to the addition, deletion,
      and presence of multicast groups.
