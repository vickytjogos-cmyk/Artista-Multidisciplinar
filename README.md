# Artista-Multidisciplinar
import { motion } from 'framer-motion';
import { FaPaintBrush, FaPencilAlt, FaLaptop, FaTheaterMasks, FaMicrophoneAlt, FaFilm, FaFeatherAlt, FaScissors, FaTshirt, FaMusic, FaBrain, FaCamera } from 'react-icons/fa';
import { GiLipstick, GiSewingNeedle, GiDramaMasks, GiDancer } from 'react-icons/gi';

export default function ColetivoArtistico() {
  const secoes = [
    { icon: <FaPaintBrush />, titulo: 'Pintura Tradicional', texto: 'Exploramos o gesto e a textura. A pintura é o ponto de partida — o caos transformado em cor.' },
    { icon: <FaPencilAlt />, titulo: 'Desenho', texto: 'O traço é a primeira linguagem do artista. Do esboço técnico ao traço expressivo que revela o invisível.' },
    { icon: <FaLaptop />, titulo: 'Ilustração Digital', texto: 'Do analógico ao pixel — criamos universos e atmosferas. Cada camada é uma história.' },
    { icon: <GiLipstick />, titulo: 'Maquiagem Artística', texto: 'Transformamos pessoas em obras vivas. Bodypaint, caracterização e efeitos especiais.' },
    { icon: <GiSewingNeedle />, titulo: 'Costura e Figurino', texto: 'Tecidos ganham vida. Criamos roupas e expressões de identidade.' },
    { icon: <FaTshirt />, titulo: 'Produção de Cosplay', texto: 'Do conceito ao acabamento. O corpo é nossa tela e o personagem, nossa arte.' },
    { icon: <GiDancer />, titulo: 'Dança', texto: 'Jazz, street, ballet. O corpo fala, vibra e comunica energia pura.' },
    { icon: <GiDramaMasks />, titulo: 'Atuação Teatral', texto: 'Vivemos outras vidas para expressar a nossa. O palco é o espelho do mundo.' },
    { icon: <FaMicrophoneAlt />, titulo: 'Dublagem e Canto', texto: 'A voz atua, canta e emociona. É som, ritmo e alma.' },
    { icon: <FaFilm />, titulo: 'Produção Audiovisual', texto: 'Filmagem, direção, edição e narrativa. Contamos histórias com movimento.' },
    { icon: <FaFeatherAlt />, titulo: 'Escrita Criativa', texto: 'Roteiros, poemas e personagens — palavras que constroem mundos.' },
    { icon: <FaBrain />, titulo: 'Criação de Personagens', texto: 'Construímos identidades artísticas únicas — simbólicas e humanas.' },
    { icon: <FaCamera />, titulo: 'Direção de Arte e Estilo', texto: 'Cada detalhe comunica. Cada cor conta uma história visual.' },
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-pink-400 via-purple-500 to-indigo-600 text-white font-sans overflow-x-hidden">
      <section className="text-center py-16 px-6">
        <motion.h1 initial={{ opacity: 0, y: -30 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 1 }} className="text-5xl font-bold mb-6">
          🌈🔥 Coletivo Artístico Multidisciplinar
        </motion.h1>
        <p className="max-w-2xl mx-auto text-lg italic">
          Somos artistas que trabalham com o corpo, a imagem, a voz, a fantasia, a realidade, o drama, a beleza, o caos e a delicadeza. <br />
          Estúdio, palco, passarela, tela e espelho. Tudo junto, tudo misturado, tudo poderoso.
        </p>
      </section>

      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 px-8 pb-24">
        {secoes.map((secao, i) => (
          <motion.div
            key={i}
            initial={{ opacity: 0, y: 40 }}
            whileInView={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6, delay: i * 0.1 }}
            viewport={{ once: true }}
            className="bg-white/10 rounded-2xl p-6 shadow-lg hover:shadow-xl hover:bg-white/20 transition duration-300"
          >
            <div className="text-4xl mb-3">{secao.icon}</div>
            <h2 className="text-2xl font-semibold mb-2">{secao.titulo}</h2>
            <p className="text-sm opacity-90 leading-relaxed">{secao.texto}</p>
          </motion.div>
        ))}
      </div>

      <footer className="text-center py-10 bg-black/30">
        <motion.p initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.5 }} className="text-md italic">
          Arte é energia, é caos organizado, é revolução estética.
        </motion.p>
      </footer>
    </div>
  );
}
