// Objeto aluno
const aluno = {
  nome: "Ana Paula",
  idade: 17,
  notas: [6.5, 7.5, 8],

  calcularMedia() {
    const soma = this.notas.reduce((total, nota) => total + nota, 0);
    return soma / this.notas.length;
  }
};

// Desestruturação para acessar nome e idade
const { nome, idade } = aluno;

// Spread operator para adicionar uma nova nota ao array original
aluno.notas = [...aluno.notas, 9];

// Função para verificar a situação do aluno
function verificarSituacao(media) {
  if (media >= 7) {
    return "Aprovado ✅";
  } else {
    return "Reprovado ❌";
  }
}

// Loop para exibir todas as notas
console.log("Notas do aluno:");
for (let i = 0; i < aluno.notas.length; i++) {
  console.log(`Nota ${i + 1}:`, aluno.notas[i]);
}

// Calcula a média final
const mediaFinal = aluno.calcularMedia();

// Exibição dos resultados
console.log("Nome:", nome);
console.log("Idade:", idade);
console.log("Média final:", mediaFinal.toFixed(2));
console.log("Situação:", verificarSituacao(mediaFinal));
