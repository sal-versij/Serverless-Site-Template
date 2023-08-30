<script lang="ts">
  import { Router, Link, Route } from "svelte-routing";
  import BaseStyle from "./BaseStyle.svelte";

  import NotFound from "./pages/NotFound.svelte";
  // import LoginButton from "./components/LoginButton.svelte";
  import Home from "./pages/Home.svelte";

  // import type {FirebaseApp} from "firebase/app";

  // import AuthService from './services/AuthService.ts';
  // import FireStoreService from './services/FireStoreService.ts';
  // import type {User as AuthUser} from "firebase/auth";

  // export let app: FirebaseApp;

  // let authUser: AuthUser;
  //
  // const authService = new AuthService();
  // const fireStoreService = new FireStoreService(app);
  //
  // authService.addAuthStateChangedListener(user => authUser = user);
</script>

<BaseStyle />
<Router>
  <section class="wrapper">
    <header>
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
          <Link class="navbar-brand" to="/">Template</Link>
        </div>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon" />
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <Link class="nav-link active" to="/">Home</Link>
            </li>
          </ul>
        </div>
      </nav>
    </header>
    <main>
      <div class="container mx-auto my-3 px-3">
        <Route path="/" component={Home} />
        <!--{#if (authUser)}-->
        <!--{/if}-->
        <Route component={NotFound} />
      </div>
    </main>
    <footer class="bg-dark text-white">
      <div class="container">
        <div class="d-flex justify-content-center">
          <p class="text-center">
            © {new Date().getFullYear()} Sal-versij
          </p>
        </div>
      </div>
    </footer>
  </section>
</Router>
