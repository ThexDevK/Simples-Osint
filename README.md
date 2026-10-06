# Simples-Osint
Hi guys, iam ThexDev and i make This simples Osint exploit for you!
and you can use Only in phone and in termux!
# 1 Step
arquivo: install.sh — ele instala as dependências, cria o comando eyes em $PREFIX/bin e embutido nele está o script inteiro da ferramenta (se auto-instala direto para $PREFIX/bin, saindo da pasta de downloads para o data do Termux).
Ativação: digita eyes → pergunta só a URL → roda tudo → mostra o relatório no final.
Idioma: eyes --lang pt|en|es ou auto (padrão PT, com flag).
# 2 Step
Instalação no Termux (saindo dos Downloads para o data)
bash

pkg update -y && pkg install -y termux-setup
termux-setup-storage          # permite acessar /sdcard/Download
cp /sdcard/Download/install.sh ~/
cd ~ && bash install.sh
O instalador move tudo direto para $PREFIX/bin/eyes (que fica dentro de /data/data/com.termux/files/usr/bin — o "data" do Termux). Depois disso você pode apagar a pasta original, pois a ferramenta inteira já vive dentro do comando.
# 3 Step
eyes              # português
eyes --lang en    # English
eyes --lang es    # Español
Só digita eyes, cola a URL, e no final ele mostra o relatório completo e salva em ~/the_eyes_report_<dominio>.txt.
# O que ele coleta (simples e direto)
WHOIS — registrador, datas de criação/expiração, nameservers
DNS/IP — resolução e endereço IP
Geolocalização do IP — país, cidade, ISP
Cabeçalhos HTTP — servidor, tecnologias, cookies
Tecnologias — WordPress, Cloudflare, React, jQuery, etc.
E-mails expostos na página
Subdomínios via certificados crt.sh
Arquivos expostos — robots.txt, sitemap.xml, .env, security.txt
Portas comuns abertas (80, 443, 8080, 21, 22, 25, 3306)
