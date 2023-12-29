---
title: Honeypot Captcha, uma alternativa muito mais elegante para combater spambots
date: 2012-08-29 21:00:00 -03:00
categories:
  - Tutoriais
tags:
  - antispam
  - captcha
  - formulário
  - validação
excerpt: |-
  Em vez de fazer o usuário digitar aquela imagem chata, crie um campo que
  não é pra ser preenchido. Pode ter o mínimo de tamanho e depois torne-o invisível
  com {display:none;}...
img: /img/css-abbreviations.jpg
---

<blockquote>
  <div class="horizontal center">
    <div style="flex: 1 1 40%">
      <img src="data:image/png;base64,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" alt="CAPTCHA"/>
    </div>
    <div style="flex: 1 1 60%">
      <p>Além da grande barreira de acessibilidade, já que os CAPTCHAs tradicionais não costumam ser acessíveis, novas modalidades de CAPTCHA mais difíceis vem sendo criados para evitar que robôs consigam acessar seus formulários.</p>
      <p><small>Reinaldo Ferraz, em <a href="http://tableless.com.br/eu-nao-sou-uma-maquina/" target="_blank" title="Tableless / Acessibilidade">Eu não sou uma máquina</a></small></p>
    </div>
  </div>
</blockquote>

Honeypot Captcha é o nome dado a uma técnica para evitar o preenchimento de formulários por <em lang="en">spambots</em>, sem que o usuário tenha que fazer nenhum esforço adicional para provar que é um ser humano. Em vez de fazer o usuário digitar aquela imagem chata, crie um campo que <strong>não é pra ser preenchido</strong>. Pode ter o mínimo de tamanho e depois torne-o invisível com <code>{display:none;}</code>.
 
Quando o <em lang="en">spambot</em> tentar mandar uma mensagem, ele não terá como saber o que é aquele campo, então o preencherá e por isso será bloqueado. Sem o usuário ser incomodado.
 
<a href="http://jsfiddle.net/johnylab/qEy75/" target="_blank">Veja um exemplo de Honeypot Captcha.</a>
 
Antes do botão de Enviar Mensagem, tem um campinho de input no HTML, que só um spambot verá, pois fica oculto para o usuário através do CSS. Ao receber uma submissão do formulário, o servidor verifica se este campo está vazio. Se não, uma página de erro "Não foi possível..." é exibida, sem ser enviada nenhuma informação. Pronto, fim do CAPTCHA pra sempre.
 
Mais detalhes (em inglês):
<a href="http://haacked.com/archive/2007/09/11/honeypot-captcha.aspx" target="_blank">Honeypot Captcha - You’ve Been Haacked</a>