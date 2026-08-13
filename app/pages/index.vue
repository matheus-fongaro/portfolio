<template>
    <div>
        <header
            class="bg-blueprint pt-32 pb-20 md:pt-40 md:pb-32 px-4 relative overflow-hidden text-center md:text-left border-b-4 border-eng-light">
            <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between relative z-10">
                <div class="md:w-3/5 text-white pr-0 md:pr-10">
                    <span class="text-eng-light font-semibold tracking-wider text-sm uppercase mb-4 block">Parceria
                        Estratégica B2B</span>
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Escale seu escritório
                        terceirizando <span class="text-eng-light">projetos complementares</span>.</h1>
                    <p class="text-gray-300 text-lg md:text-xl mb-8 max-w-2xl mx-auto md:mx-0">
                       Aumente sua capacidade de entrega enquanto cuido de todo o desenvolvimento técnico. Entrego
                        projetos elétricos e hidrossanitários 100% compatibilizados em BIM.
                    </p>
                    <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                       <NuxtLink to="#contato"
                            class="bg-eng-light text-eng-dark px-8 py-4 rounded-md font-bold hover:bg-white transition-all transform hover:-translate-y-1 shadow-lg text-center">
                            Discutir uma Parceria</NuxtLink>
                       <NuxtLink to="#portfolio"
                            class="bg-transparent border border-eng-light text-eng-light px-8 py-4 rounded-md font-bold hover:bg-eng-light hover:text-eng-dark transition-all text-center">
                            Ver Trabalhos</NuxtLink>
                    </div>
                </div>
                <!-- Hero graphic -->
                <div class="md:w-2/5 mt-12 md:mt-0 hidden md:block">
                    <div class="relative w-full max-w-md mx-auto aspect-square">
                        <!-- Decorative elements simulating 3D modeling -->
                        <div
                            class="absolute inset-0 border-2 border-eng-light opacity-20 rounded-lg transform rotate-6">
                        </div>
                        <div
                            class="absolute inset-0 border-2 border-eng-light opacity-50 rounded-lg transform -rotate-3">
                        </div>
                       <NuxtImg src="/Modelo 3d.png" alt="Representação BIM"
                            class="rounded-lg shadow-2xl relative z-10 object-cover w-full h-full border border-eng-accent" />
                    </div>
                </div>
            </div>
        </header>

        <section class="bg-white py-12 border-b border-gray-200">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div
                    class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center divide-y md:divide-y-0 md:divide-x divide-gray-200">
                    <IconWithText icon="lucide:clock" title="Entregas Rápidas"
                        description="Respeito rigoroso aos prazos para não atrasar o cronograma do seu escritório." />
                    <IconWithText icon="lucide:shield-check" title="Zero Retrabalho (BIM)"
                        description="Compatibilização completa para evitar conflitos no canteiro de obras." />
                    <IconWithText icon="lucide:circle-dollar-sign" title="Redução de Custos"
                        description="Terceirize sob demanda. Custo fixo zero com ociosidade da equipe técnica." />
                </div>
            </div>
        </section>

        <section id="servicos" class="py-20 bg-eng-gray">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <SectionTitle title="Soluções Técnicas para o seu Escritório"
                    description="Especialidade em projetos executivos limpos, normatizados e prontos para a obra, com foco em residências e edificações comerciais." />
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <ServiceDescriptionCard icon="mdi:home-lightning-bolt" title="Projeto Elétrico" description="Dimensionamento preciso de cargas, quadros de distribuição, tomadas e
                        iluminação. Prevenção contra curtos e otimização de materiais (fios e conduítes), totalmente em
                        conformidade com a NBR 5410."
                        :items="['Diagrama Unifilar Automático', 'Lista de Materiais Exata']" />
                    <ServiceDescriptionCard icon="mdi:water-pump" title="Projeto Hidrossanitário" description="Água fria, água quente, esgoto e águas pluviais. Detalhamento
                        isométrico de banheiros e cozinhas em BIM para garantir que a tubulação não interfira na
                        estrutura ou no design arquitetônico."
                        :items="['Isométricas em 3D', 'Prevenção de Infiltrações']" />
                    <ServiceDescriptionCard icon="mdi:video-3d" title="Modelagem 3D e Compatibilização BIM"
                        description="Transformo seus esboços em modelos BIM completos no Revit e crio
                        renderizações fotorrealistas de alto impacto visual, facilitando a visualização e compatibilização do projeto." :items="['Modelos 3D Detalhados', 'Resolução de Conflitos']" />
                </div>
            </div>
        </section>

        <section id="portfolio" class="py-20 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <SectionTitle title="Estudos de Caso & Entregas"
                    description="Exemplos reais de como a engenharia bem aplicada protege o projeto arquitetônico e otimiza a obra." />
                <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                   <PortfolioCard image="/hidro.png" tag="Hidrossanitário"
                        title="Residência Unifamiliar - Detalhamento Isométrico">
                        <p class="text-gray-600 mb-4 text-sm line-clamp-3">
                            <strong class="text-eng-dark">Desafio:</strong> Suíte e área de lavanderia em um espaço
                            amplo<br>
                            <strong class="text-eng-dark">Solução:</strong> Modelagem 100% em Revit com desvios precisos
                            e entrega de vistas isométricas detalhadas para o encanador.
                        </p>
                    </PortfolioCard>
                   <PortfolioCard image="/eletrico.png" tag="Elétrico" title="Projeto Elétrico Inteligente">
                        <p class="text-gray-600 mb-4 text-sm line-clamp-3">
                            <strong class="text-eng-dark">Desafio:</strong> Adequação do projeto elétrico à demandas
                            específicas de equipamentos do cliente, incluindo circuitos para refrigeração.<br>
                            <strong class="text-eng-dark">Solução:</strong> Circuitos balanceados, demanda presente e
                            futura calculada.
                        </p>
                    </PortfolioCard>
                   <PortfolioCard image="render.png" tag="Render & BIM" title="Apresentação Fotorrealista para Venda">
                        <p class="text-gray-600 mb-4 text-sm line-clamp-3">
                            <strong class="text-eng-dark">Desafio:</strong> Renderização de imagens de alto impacto para
                            apresentação.<br>
                            <strong class="text-eng-dark">Solução:</strong> Importação do projeto arquitetônico,
                            aplicação
                            de texturas e iluminação realista. Aprovação de primeira.
                        </p>
                    </PortfolioCard>
                   <PortfolioCard image="clash.png" tag="Compatibilização"
                        title="Compatibilização e Prevenção de Clashes">
                        <p class="text-gray-600 mb-4 text-sm line-clamp-3">
                            <strong class="text-eng-dark">O Valor do BIM:</strong> Identificação virtual de um tubo de
                            esgoto de 100mm que atravessaria uma viga principal. O problema foi resolvido no modelo 3D
                            antes da concretagem, economizando tempo e dinheiro em retrabalho na obra.
                        </p>
                    </PortfolioCard>
                </div>
            </div>
        </section>

        <section id="sobre" class="py-20 bg-eng-dark text-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-col md:flex-row items-center gap-12">
                    <Reveal class="md:w-1/2">
                        <div
                            class="relative w-64 h-64 mx-auto md:mx-0 rounded-full border-4 border-eng-light overflow-hidden shadow-2xl">
                           <NuxtImg src="/selfie.png" class="w-full h-full object-cover" />
                        </div>
                    </Reveal>
                    <Reveal class="md:w-1/2 text-center md:text-left delay-100">
                        <h2 class="text-3xl md:text-4xl font-bold mb-4">Engenheiro Parceiro do seu Negócio</h2>
                        <div class="h-1 w-20 bg-eng-light mx-auto md:mx-0 mb-6"></div>
                        <p class="text-gray-300 text-lg mb-6 leading-relaxed">
                            Sou Engenheiro Civil, atuando ativamente como prestador de serviços técnicos em Cacoal/RO e
                            de
                            forma remota para escritórios de todo o Brasil.
                        </p>
                        <p class="text-gray-300 text-lg mb-6 leading-relaxed">
                            Meu foco não é competir com profissionais da construção civil, mas sim ser a
                            <strong>retaguarda
                                técnica</strong>.
                           Entendo a fundo os softwares mais modernos do mercado, as normas vigentes e as melhores
                            práticas para garantir que sua
                            concepção arquitetônica não tenha problemas na hora de ser construída.
                        </p>
                        <div class="grid grid-cols-2 gap-4 text-sm font-semibold">
                            <div class="flex items-center">
                                <Icon name="mdi:check-circle" class="w-5 h-5 text-eng-light mr-2" />
                                Disponível para trabalho remoto
                            </div>
                            <div class="flex items-center">
                                <Icon name="mdi:check-circle" class="w-5 h-5 text-eng-light mr-2" />
                                Parcerias com Comissionamento
                            </div>
                        </div>
                    </Reveal>
                </div>
            </div>
        </section>

        <section id="contato" class="py-20 bg-eng-gray relative">
            <Reveal class="max-w-2xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="bg-white rounded-2xl shadow-xl overflow-hidden flex flex-col md:flex-row">
                    <div class="bg-eng-primary text-white p-10 flex flex-col justify-center">
                        <h3 class="text-2xl font-bold mb-4 text-center">Vamos conversar sobre sua próxima demanda?</h3>
                        <p class="text-gray-300 mb-8 text-sm text-center">Me chame no WhatsApp para analisarmos o
                            projeto do
                            seu
                            cliente. <br> Respondo com propostas e prazos rapidamente.</p>
                        <NuxtLink to="https://wa.me/5569920005386" target="_blank"
                            class="flex items-center justify-center gap-3 bg-green-500 text-white py-4 px-6 rounded-lg font-bold hover:bg-green-600 transition-colors shadow-lg">
                            <Icon name="mdi:whatsapp" class="w-6 h-6" /> Contato via WhatsApp
                        </NuxtLink>
                    </div>
                </div>
            </Reveal>
        </section>

        <footer class="bg-eng-dark text-gray-400 py-8 border-t border-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0 text-center md:text-left">
                    <span class="font-bold text-xl tracking-tight text-white">Matheus Fongaro <span
                            class="text-eng-light">Engenheiro Civil</span></span>
                    <p class="text-sm mt-1">Cacoal/RO - Atendimento Remoto Nacional</p>
                </div>
                <div class="text-sm text-center">
                    &copy; {{ new Date().getFullYear() }} Matheus Fongaro. Todos os direitos reservados.
                </div>
            </div>
        </footer>
    </div>
</template>