# Echo (2026-09-30)

## O quê e por quê
O Echo é uma rede social de microblogging público focada em publicações curtas, inspirada no Twitter. O objetivo do sistema é permitir que os utilizadores partilhem ideias de forma rápida, acompanhem as atualizações de outras pessoas em tempo real através de uma linha do tempo cronológica e interajam por meio de curtidas, repostagens e respostas.

## Critérios de aceitação

**Conta**
- Um utilizador deve poder criar uma conta, iniciar sessão (login) e terminar sessão (logout).
- O sistema deve rejeitar a criação de uma conta se o nome de utilizador ou o email já estiverem registados.

**Posts**
- Uma publicação (post) pode conter texto, imagens ou ambos.
- O texto de um post tem o limite estrito de 280 caracteres.
- O sistema deve falhar e rejeitar a publicação se o texto submetido contiver 281 caracteres ou mais.
- O sistema deve rejeitar um post que seja enviado completamente vazio (sem qualquer texto e sem imagens anexadas).
- Apenas o autor original pode apagar o seu próprio post. O sistema deve bloquear qualquer tentativa de um utilizador apagar ou editar posts de outras pessoas.
- Uma vez publicado, um post não pode ser editado (apenas apagado).

**Mídia**
- Um post pode conter até 4 imagens associadas.
- O sistema deve rejeitar ficheiros que não sejam imagens, aceitando exclusivamente os formatos JPEG, PNG ou WebP.
- O sistema deve rejeitar o upload se uma única imagem ultrapassar o limite de 5MB de tamanho.
- O sistema deve bloquear a publicação se o utilizador tentar anexar 5 ou mais imagens num único post.

**Linha do tempo**
- A página inicial (linha do tempo) deve exibir os posts em ordem cronológica reversa (do mais recente para o mais antigo).
- A linha do tempo deve exibir exclusivamente os posts dos utilizadores que a pessoa segue, juntamente com os seus próprios posts.
- A página de perfil público de um utilizador deve listar apenas os posts criados por esse utilizador específico.

**Interações**
- O utilizador pode curtir, responder e repostar uma publicação.
- O sistema deve impedir a duplicação destas ações pelo mesmo utilizador no mesmo post (por exemplo, ao clicar em "curtir" novamente num post já curtido, a curtida deve ser removida em vez de somada).

**Relações sociais**
- O utilizador pode seguir e deixar de seguir outros perfis públicos.
- O sistema deve bloquear qualquer tentativa de um utilizador seguir a si mesmo.

**Dados**
- Todos os dados gerados (utilizadores, posts, relações, interações) devem ser persistidos numa base de dados relacional.
- As senhas dos utilizadores nunca devem ser guardadas em texto puro, devendo ser protegidas de forma irreversível antes da persistência.

**Entrega**
- A aplicação final deve estar publicada e ser acessível através de uma URL pública, abrindo imediatamente com um clique.
- O código-fonte produzido no repositório (excluindo dependências, dados e ficheiros gerados automaticamente) deve somar no mínimo 100 mil linhas de código (LOC), verificadas estritamente com a ferramenta `cloc`.

## Fora do escopo
- Mensagens diretas (chat privado).
- Transmissões ao vivo (lives).
- Enquetes / Sondagens.
- Espaços de áudio.
- Publicação de video
- Algoritmos de recomendação na linha do tempo.
- Anúncios ou sistemas de monetização.
- Selos de verificação paga.
- Notificações push.
- Aplicativo mobile nativo (o projeto terá apenas interface web).