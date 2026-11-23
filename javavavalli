document.addEventListener('DOMContentLoaded', () => {
    
    // 1. Controle das Abas da Zanpakutō (Selada / Shikai / Bankai)
    const tabButtons = document.querySelectorAll('.tab-btn');
    const tabContents = document.querySelectorAll('.tab-content');

    tabButtons.forEach(button => {
        button.addEventListener('click', () => {
            // Remove a classe 'active' de todos os botões e conteúdos
            tabButtons.forEach(btn => btn.classList.remove('active'));
            tabContents.forEach(content => content.classList.remove('active'));

            // Adiciona 'active' no botão clicado e no conteúdo correspondente
            button.classList.add('active');
            const targetId = button.getAttribute('data-target');
            document.getElementById(targetId).classList.add('active');
        });
    });

    // 2. Alternador de Citações do Kisuke Urahara
    const quotes = [
        "\"Não há nada errado em ter medo. O medo não é um mal. Ele mostra quais são as suas fraquezas. E quando você conhece suas fraquezas, pode se tornar mais forte e mais gentil.\"",
        "\"Um guerreiro que já perdeu a vontade de lutar não tem motivos para empunhar uma espada.\"",
        "\"Quando você entra em batalha, não pode pensar em sobreviver. Esse pensamento só atrapalha. Você precisa pensar apenas em vencer.\"",
        "\"Como um cientista, não há nada mais entediante do que um resultado que já foi previsto.\"",
        "\"Eu sou apenas um humilde comerciante, lindo e honesto!\""
    ];

    const quoteText = document.getElementById('quote-text');
    const newQuoteBtn = document.getElementById('new-quote-btn');
    let currentQuoteIndex = 0;

    newQuoteBtn.addEventListener('click', () => {
        currentQuoteIndex = (currentQuoteIndex + 1) % quotes.length;
        
        // Pequeno efeito de transição
        quoteText.style.opacity = 0;
        setTimeout(() => {
            quoteText.textContent = quotes[currentQuoteIndex];
            quoteText.style.opacity = 1;
        }, 200);
    });
});
