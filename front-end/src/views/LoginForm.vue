<template>
    <header class="header">
      <img :src="require('@/assets/setima_logo.png')" alt="LOGO-ECONOTIFICA" class="logo">
    </header>
    <div id="app" class="login-container">
      <div class="overlay"></div>
      <div class="content">
          <img :src="require('@/assets/image_planet.png')" alt="Earth" class="globe-img"/>
        <form class="login-form">
          <h2>Login</h2>
          <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" placeholder="exemple@gmail.com" />
          </div>
          <div class="form-group">
            <label for="password">Senha:</label>
            <input type="password" id="password" placeholder="******" />
          </div>
          <a href="#" class="forgot-password">Esqueceu a senha?</a>
          <button type="submit" class="btn-login">ENTRAR</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "LoginForm",
  };
  </script>
  
  
  
  <style>
  html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    
  }
  
  #app {
    width: 100%;
    height: 100%;
  }
  </style>
  
  
  
  <style scoped>
  
  .logo {
  max-width:300px; /* Ajuste o tamanho do logo */
  height: auto;
  margin: 0 auto;
  display: block;
  filter: drop-shadow(4px 4px 6px rgba(0, 0, 0, 1)); /* Sombra ajustada ao contorno */
}
  /* Estilo principal */
  .login-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    /*background: linear-gradient(to bottom, #2e2e2e, #1a1a1a);*/
    background: url('@/assets/image_fundo.jpg') no-repeat center center;
    background-size: 90% auto;
    background-position: center; 
    font-family: Arial, sans-serif;
    color: #fff;
    position: relative;
    width: 100px;
  
  }
  
  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5); 
    z-index: 0; 
  }
  
  /* Header */
  .header {
    background:  linear-gradient(to bottom, #016126, #06DB58, #03e75b);
    width: 100%;
    padding: 20px 0;
    text-align: center;
    position: relative;
    top: 0;
  }
  
  .header h1 {
    margin: 0;
    font-size: 2.5rem;
    color: white;
  }
  
  /* Conteúdo */
  .content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    gap: 30px;
    margin-top: 40px;
    margin-right: 90px;
    z-index: 1;
  }
  
  /*ANIMAÇÃO DA IMAGEM DA TERRA*/
  @keyframes float {
    0% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-10px);
    }
    100% {
      transform: translateY(0);
    }
  }
  
  
  /* Globo */
  .globe img {
    border-radius: 50%;
    width: 500px;
    height: 500px;
    object-fit: cover;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
    animation: float 5s ease-in-out infinite;
  }
  .globe-img {
    border-radius: 50%;
    width: 500px;
    height: 500px;
    object-fit: cover;
    /*box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);*/
    animation: float 5s ease-in-out infinite;
  }
  
  /* Formulário */
  .login-form {
    background-color: rgba(0, 0, 0, 0.6);
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    width: 300px;
    z-index: 1;
  }
  
  .login-form h2 {
    text-align: center;
    margin-bottom: 20px;
    color: #fff;
    font-size: 1.5rem;
  }
  
  .form-group {
    margin-bottom: 15px;
    width: 285px;
  }
  
  .form-group label {
    display: block;
    margin-bottom: 5px;
    font-size: 1rem;
    color: #ccc;
  }
  
  .form-group input {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    font-size: 1rem;
    background-color: #fff;
  }
  
  .forgot-password {
    display: block;
    margin: 10px 0;
    text-align: right;
    font-size: 0.9rem;
    color: #ccc;
    text-decoration: none;
  }
  
  .forgot-password:hover {
    text-decoration: underline;
  }
  
  /* Botão */
  .btn-login {
    width: 100%;
    padding: 10px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 1.1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .btn-login:hover {
    background-color: #218838;
  }
  </style>
  