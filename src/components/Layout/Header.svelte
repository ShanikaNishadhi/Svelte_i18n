<!-- <script>
    import { _ } from '../../services/i18n';
</script>

<header class="hero">
    <div class="hero-body">
        <div class="contiainer">
            <h1 class="title">{$_('app.title')}</h1>

            <h2 class="subtitle">{$_('app.subtitle')}</h2>
        </div>
    </div>
</header> -->
<script>
  import { _ } from '../../services/i18n';
  import { Link } from "svelte-routing";
  import "../../../node_modules/materialize-css/dist/css/materialize.min.css";
</script>

<nav>
  <div class="nav-wrapper">
    <div class="container">
      <Link to="/">
        <span class="brand-logo">{$_('home.topic')}</span>
      </Link>
    </div>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li>
          <Link to="/pluralization">Home</Link>
        </li>
        <li>
          <Link to="/about">About</Link>
        </li>
        <li>
          <Link to="/contact">Contact Us</Link>
        </li>
      </ul>
    </div>
</nav>