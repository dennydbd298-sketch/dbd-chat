# DBD Chat Ultimate Black

## IMPORTANTE — por que o botão enviar não funcionava

O `index.html` **não pode ser aberto diretamente pelo gestor de ficheiros do Android**. Quando o navegador mostra um endereço começando por `content://media/external/...`, ele está a abrir um ficheiro local. Nesse modo não existe o servidor Flask em `/api/chat`, `/api/me`, etc.; por isso a mensagem não é enviada.

### Para usar online
Publique esta pasta num serviço compatível com Flask (por exemplo Render/Railway) e configure as variáveis do `.env.example`. Depois abra o endereço `https://...` fornecido pelo serviço.

### Para testar num computador
```bash
pip install -r requirements.txt
python run_local.py
```
Depois abra `http://127.0.0.1:5000`.

## APIs necessárias
- `GEMINI_API_KEY` para chat/pesquisa/imagem/vídeo.
- `GOOGLE_CLIENT_ID` para Google Login.
- `FACEBOOK_APP_ID` e `FACEBOOK_APP_SECRET` para Facebook Login.
- `X_CLIENT_ID` e `X_CLIENT_SECRET` para X Login.

As credenciais devem ficar no servidor, nunca num HTML público.
