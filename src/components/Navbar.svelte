<script>
  import {
    LoginScreen,
    Page,
    LoginScreenTitle,
    List,
    Button,
    ListInput,
    ListButton,
    f7,
    Navbar,
    Link
  } from "framework7-svelte";

  let loginScreenOpened = false;
  let username = "";
  let password = "";
  const validUsername = "DoorsTickets";
  const validPassword = "123456";

  function signIn() {
    if (username === validUsername && password === validPassword) {
      // Las credenciales son válidas
      f7.dialog.alert("Inicio de sesión exitoso", () => {
        f7.loginScreen.close();
      });
    } else {
      // Las credenciales son incorrectas
      f7.dialog.alert("Credenciales incorrectas. Inténtelo de nuevo.");
    }
  }

  function goBack() {
    // Cierra la pantalla de inicio de sesión y vuelve a la vista anterior
    f7.loginScreen.close();
  }

  let src = "icons/doors.png";
</script>

<Navbar>
  <div class="navbar-inner">
    <div class="left">
      <Link>
        <img {src} alt="logo" class="logo" />
      </Link>
    </div>

    <div class="nav-links">
      <a href="/">Inicio</a>
      <a href="/">Acerca</a>
      <a href="/">Contacto</a>
      <a href="/">Soporte</a>
    </div>

    <div class="right login-btn">
      <a href="/" on:click={() => (loginScreenOpened = true)}>Ingresar</a>
      <Button type="button" fill>Crear Cuenta</Button>
    </div>
  </div>
</Navbar>

<LoginScreen
  class="demo-login-screen"
  opened={loginScreenOpened}
  onLoginScreenClosed={() => {
    loginScreenOpened = false;
  }}
>
  <Page loginScreen>
    <div class="navbar">
      <div class="navbar-inner sliding">
        <div class="left">
          <Button iconF7="arrow_left" class="back" onClick={goBack}></Button>
        </div>
      </div>
    </div>
    <LoginScreenTitle>Iniciar Sesion</LoginScreenTitle>
    <List form>
      <ListInput
        label="Username"
        type="text"
        placeholder="Your username"
        value={username}
        onInput={(e) => (username = e.target.value)}
      />
      <ListInput
        label="Password"
        type="password"
        placeholder="Your password"
        value={password}
        onInput={(e) => (password = e.target.value)}
      />
    </List>
    <List inset>
      <ListButton onClick={signIn}>Sign In</ListButton>
    </List>
  </Page>
</LoginScreen>

