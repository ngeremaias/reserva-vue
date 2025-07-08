<template>
  <nav class="navbar">
    <div class="logo">RESERV<span>A</span></div>
    <ul class="menu">
      <li><a href="#">Início</a></li>
      <li><a href="#">Para Proprietários</a></li>
      <li><a href="#">Sobre Nós</a></li>
      <li><a href="#">Contato</a></li>
    </ul>
    <div class="auth">
      <button class="create">Criar conta</button>
      <button class="login">Entrar</button>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background: black;
  color: white;
  display: flex;
  justify-content: space-between;
  padding: 1rem 2rem;
  align-items: center;
}
.logo {
  color: #C5FD01;
  font-weight: bold;
  font-size: 1.5rem;
}
.menu {
  display: flex;
  list-style: none;
  gap: 1rem;
}
.menu a {
  color: white;
  text-decoration: none;
}
.auth button {
  margin-left: 10px;
  padding: 0.5rem 1rem;
}
.create {
  background: #C5FD01;
  border: none;
}
.login {
  background: white;
  border: none;
}
</style>