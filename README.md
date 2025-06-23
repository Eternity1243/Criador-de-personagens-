# 🎮 Criador de Personagens Simples

Este é um projeto web simples de "Criador de Personagens", desenvolvido com HTML, CSS e JavaScript puro. Ele permite aos usuários selecionar um nome, classe, cor da roupa e arma para gerar uma ficha básica de personagem.

## 🚀 Como Usar

1.  **Acesse a página:** Você pode ver o projeto funcionando diretamente no GitHub Pages através deste link:
    `https://SEU-USUARIO.github.io/SEU-NOME-DO-REPOSITORIO/`
    *(Lembre-se de substituir `SEU-USUARIO` pelo seu nome de usuário do GitHub e `SEU-NOME-DO-REPOSITORIO` pelo nome que você deu ao seu repositório, como `criador-de-personagens`).*

2.  **Preencha os campos:** Digite um nome e selecione as opções desejadas nos menus suspensos (classe, cor da roupa, arma).

3.  **Crie o personagem:** Clique no botão "Criar Personagem" para gerar a ficha abaixo.

## 💻 Código Fonte

Você pode visualizar e explorar o código completo do projeto abaixo.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Criador de Personagens</title>
  <style>
    body { font-family: Arial; background-color: #f0f0f0; padding: 20px; }
    label, select, input { display: block; margin: 10px 0; }
    #ficha { margin-top: 20px; padding: 10px; background: #fff; border: 1px solid #ccc; }
  </style>
</head>
<body>
  <h1>🎮 Criador de Personagens</h1>

  <label>Nome: <input type="text" id="nome"></label>

  <label>Classe:
    <select id="classe">
      <option>Mago</option>
      <option>Guerreiro</option>
      <option>Arqueiro</option>
      <option>Ninja</option>
    </select>
  </label>

  <label>Cor da roupa:
    <select id="cor">
      <option>Azul</option>
      <option>Vermelha</option>
      <option>Verde</option>
      <option>Preta</option>
    </select>
  </label>

  <label>Arma:
    <select id="arma">
      <option>Espada</option>
      <option>Cajado</option>
      <option>Arco</option>
      <option>Shuriken</option>
    </select>
  </label>

  <button onclick="criarPersonagem()">Criar Personagem</button>

  <div id="ficha"></div>

  <script>
    function criarPersonagem() {
      const nome = document.getElementById('nome').value;
      const classe = document.getElementById('classe').value;
      const cor = document.getElementById('cor').value;
      const arma = document.getElementById('arma').value;

      const ficha = `
        <h2>Ficha do Personagem</h2>
        <p><strong>Nome:</strong> ${nome}</p>
        <p><strong>Classe:</strong> ${classe}</p>
        <p><strong>Cor da roupa:</strong> ${cor}</p>
        <p><strong>Arma:</strong> ${arma}</p>
      `;

      document.getElementById('ficha').innerHTML = ficha;
    }
  </script>
</body>
</html>
