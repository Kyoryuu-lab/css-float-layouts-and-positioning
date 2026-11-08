<h1>css-float-layouts-and-positioning</h1>
<p>Deep dive into CSS floating mechanics, Block Formatting Contexts (BFC), clear-fix techniques, centered floating menus, and Bootstrap 4 integration</p>

<h2>Project description</h2>
<p>This project provides an empirical and structural exploration of traditional CSS layout algorithms and positioning mechanics before the widespread adoption of Flexbox and Grid:</p>
<ol>
  <li>
    <dl>
      <dt><b>Float Mechanics &amp; Text Wrapping:</b></dt>
      <dd>Examines bidirectional floating (<code>float: left</code>, <code>float: right</code>) and boundary wrapping behaviors around inline block containers.</dd>
      <dd>Demonstrates coordinate shifting via negative margins (e.g. <code>margin-left: -4em</code>) to create layered text overlays.</dd>
    </dl>
  </li>
  <li>
    <dl>
      <dt><b>Block Formatting Context (BFC) &amp; Float Containment:</b></dt>
      <dd>Resolves parent height collapse caused by floating children using the <code>overflow: hidden</code> BFC generation technique.</dd>
      <dd>Applies directional clearing (<code>clear: left</code>) to isolate subsequent document flow from floated siblings.</dd>
    </dl>
  </li>
  <li>
    <dl>
      <dt><b>Horizontal Float Centering (Double-Relative Technique):</b></dt>
      <dd>Implements the classic 50% / -50% relative positioning pattern to center floated lists of unknown width without table hacks.</dd>
    </dl>
  </li>
  <li>
    <dl>
      <dt><b>Modern Bootstrap 4 Integration:</b></dt>
      <dd>Integrates a complete local distribution of Bootstrap v4.4.1 (including jQuery 3.4.1 and Popper.js) to provide a responsive overview portal.</dd>
    </dl>
  </li>
</ol>

<h2>Project files</h2>
<table>
  <tr>
    <th colspan="2">css-float-layouts-and-positioning</th>
  </tr>
  <tr>
    <td>index.html</td>
    <td>Responsive dashboard portal styled with Bootstrap 4 linking to all layout experiments</td>
  </tr>
  <tr>
    <td>pages/float-text-flow.html</td>
    <td>Interactive demo of float flow, negative margins, clear breaks, and BFC containment</td>
  </tr>
  <tr>
    <td>pages/float-centered-menu.html</td>
    <td>Demonstration of the double-relative horizontal centering technique for float menus</td>
  </tr>
  <tr>
    <td>css/float-text-flow.css</td>
    <td>Stylesheet isolating float positioning, margin offsets, and overflow rules[span_21]</td>
  </tr>
  <tr>
    <td>css/float-centered-menu.css</td>
    <td>Stylesheet implementing relative coordinate offsets and list navigation styling</td>
  </tr>
  <tr>
    <td>vendor/</td>
    <td>Local dependencies containing Bootstrap 4.4.1, jQuery 3.4.1, and Popper.js</td>
  </tr>
  <tr>
    <td>README.md</td>
    <td>Project documentation and architectural overview</td>
  </tr>
  <tr>
    <td>.gitignore</td>
    <td>Exclusion rules for editor caches and operating system metadata</td>
  </tr>
</table>

<h2>Layout Mechanics Comparison</h2>
<table>
  <tr>
    <th>Technique</th>
    <th>CSS Properties</th>
    <th>Functional Behavior</th>
  </tr>
  <tr>
    <td><b>BFC Containment</b></td>
    <td><code>overflow: hidden;</code></td>
    <td>Forces parent container to expand and encompass all floated children without collapsing</td>
  </tr>
  <tr>
    <td><b>Directional Clear</b></td>
    <td><code>clear: left;</code></td>
    <td>Pushes element below any preceding left-floated elements</td>
  </tr>
  <tr>
    <td><b>Centered Float</b>x</td>
    <td><code>.wrap { left: 50%; } #menu { left: -50%; }</code></td>
    <td>Symmetrically balances unknown-width float menus across the viewport center</td>
  </tr>
  <tr>
    <td><b>Negative Margin Offset</b></td>
    <td><code>margin-left: -4em;</code></td>
    <td>Pulls inline float into the spatial bounding box of the previous sibling</td>
  </tr>
</table>

<h2>Installation and launch</h2>
<ol>
  <b>
    <li>
      <dl>
        <dt>Clone repository</dt>
        <dd>
          <code>git clone https://github.com/Kyoryuu-lab/css-float-layouts-and-positioning.git</code>
        </dd>
        <dd>
          <code>cd css-float-layouts-and-positioning</code>
        </dd>
      </dl>
    </li>
  </b>
  <b>
    <li>
      <dl>
        <dt>View locally</dt>
        <dd>Open <code>index.html</code> directly in any web browser:</dd>
        <dd>
          <code>open index.html</code> &nbsp;(macOS) &nbsp;oder&nbsp; <code>xdg-open index.html</code> &nbsp;(Linux)
        </dd>
      </dl>
    </li>
  </b>
  <b>
    <li>
      <dl>
        <dt>Run via lightweight local web server</dt>
        <dd>
          <code>python3 -m http.server 8080</code>
        </dd>
        <dd>Navigate to: <code>http://localhost:8080</code></dd>
      </dl>
    </li>
  </b>
</ol>
