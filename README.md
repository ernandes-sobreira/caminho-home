# Rota Home Care 🚑

Aplicativo web para planejamento de visitas domiciliares de equipes de Home Care, com mapa e navegação no navegador.

## Acessar o aplicativo

Depois de ativar o **GitHub Pages** para este repositório, o endereço previsto é:

**https://ernandes-sobreira.github.io/caminho-home/**

### Ativar o GitHub Pages (uma vez)

1. Abra **Settings → Pages** neste repositório.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch **main**, a pasta **/(root)** e clique em **Save**.
4. Acesse a URL acima após o GitHub indicar que o site foi publicado.

O arquivo do aplicativo está em [index.html](index.html), na raiz deste repositório. Ao atualizar esse arquivo na branch `main`, o site será atualizado pelo GitHub Pages.

## Funcionalidades

- Importação de planilha Excel (`.xlsx`) **no próprio navegador**, sem incluir os pacientes no código.
- Conversão de coordenadas geográficas em graus/minutos/segundos para latitude/longitude.
- Mapa OpenStreetMap/Leaflet, posição da ambulância via GPS e ordem sugerida de paradas por OSRM.
- Orientação de percurso em português, voz, recálculo de rota e links para Google Maps e Waze.
- Velocidade eco e estimativas de tempo, distância, CO₂ e economia em relação à ordem original da planilha.
- Cadastro de telefones, avisos de aproximação por WhatsApp/SMS **com confirmação manual do envio**.
- Correção de localização de pacientes no mapa, definição de base, simulação e exportação dos dados.

## Privacidade e segurança

**Não faça commit nem publique a planilha de pacientes.** Este repositório é público. A planilha contém informações pessoais de saúde e localização que devem ser protegidas nos termos da LGPD.

O aplicativo guarda cadastros no **localStorage** do navegador do aparelho, sem sincronização entre dispositivos. O armazenamento local não equivale a um banco de dados criptografado ou protegido por login: evite usar aparelhos compartilhados, faça backup por exportação quando apropriado e apague os dados locais quando deixarem de ser necessários.

**Importante:** ao calcular trajetos, as coordenadas das paradas são enviadas ao serviço público OSRM, e os serviços de mapas online também recebem solicitações. Portanto, não se deve interpretar o aplicativo como um sistema totalmente offline ou de sigilo integral de localização. Considere avaliação de privacidade e infraestrutura própria antes de usar dados reais de pacientes em produção.

## Limitações

- O OSRM público é demonstrativo, não tem garantia de disponibilidade e não usa trânsito em tempo real.
- GPS e certas funções do aparelho dependem de HTTPS, permissões e suporte do navegador.
- WhatsApp e SMS são abertos com texto pronto, mas **o motorista precisa tocar em enviar**; envio automático exige integração externa.
- Ainda não foram realizados testes em campo ou validação de navegação real; o aplicativo não substitui procedimentos operacionais ou de segurança de transporte de pacientes.
