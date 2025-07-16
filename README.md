import { Card, CardContent } from "@/components/ui/card";
import { Mail, Instagram } from "lucide-react";
import { motion } from "framer-motion";

// Make sure to add the Google Font link to your index.html head or _app.js
// <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&display=swap" rel="stylesheet" />

export default function YachtCopywritingPortfolioGothic() {
  return (
    <div
      className="max-w-4xl mx-auto p-6 space-y-6 bg-black text-gray-200 min-h-screen font-serif"
      style={{
        backgroundImage:
          "url('https://www.transparenttextures.com/patterns/parchment.png')",
      }}
    >
      <motion.h1
        initial={{ opacity: 0, y: -20, letterSpacing: 2 }}
        animate={{ opacity: 1, y: 0, letterSpacing: 5 }}
        transition={{ duration: 1 }}
        className="text-5xl font-bold text-center text-red-700 font-cinzel tracking-wide mb-6 underline decoration-red-800 decoration-4 underline-offset-8"
        style={{ fontFamily: "'Cinzel', serif" }}
      >
        🚤 Yacht & Boating Copywriting Portfolio
      </motion.h1>

      <motion.p
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ delay: 0.2 }}
        className="text-center text-lg text-gray-400 italic"
      >
        By Sadiq Safana – Luxury & Lifestyle Copywriter
      </motion.p>

      <motion.p
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ delay: 0.4 }}
        className="text-center italic text-gray-500"
      >
        "I help yacht brands turn cold leads into booked-out seasons — using
        storytelling, sales psychology, and high-end copywriting."
      </motion.p>

      {[...Array(7)].map((_, i) => (
        <AnimatedCardGothic
          key={i}
          title={`Email ${i + 1}: ${[
            "The Intriguing Origin Story",
            "Unique Mechanism Email",
            "Value With Sass & Personality",
            "Subtle Frustration Hook",
            "Logic + Empathy Email",
            "Sales Page Primer",
            "Urgency Closer",
          ][i]}`}
          delay={0.3 + i * 0.15}
        >
          <p>
            <strong>Subject Line:</strong>{" "}
            {[
              "I nearly sold the whole fleet.",
              "The shift that saved my charter business",
              "That 'Marketing Guru' never owned a yacht",
              "Why are you still stuck in the harbor, {{name}}?",
              "Stop wasting time on offers no one wants",
              "One wrong click rewired Sal’s yacht business",
              "Spots are sailing fast. Are you on board?",
            ][i]}
          </p>
          <p>
            <strong>Highlight:</strong>{" "}
            {[
              "Emotional storytelling + transformation arc",
              "Introduces proprietary method + clear logic for change",
              "Voice-driven, fun, anti-fluff copy",
              "Uses frustration to spark action",
              "High-ticket clarity without hustle",
              "Case study storytelling + deep transformation",
              "Bold CTA and urgency framing",
            ][i]}
          </p>
        </AnimatedCardGothic>
      ))}

      <AnimatedCardGothic title="🛟 Writing Features Showcased" delay={1.5}>
        <ul className="list-disc list-inside">
          <li>High-converting storytelling</li>
          <li>Emotional connection & clarity</li>
          <li>Nautical/luxury brand vocabulary</li>
          <li>Strategic offer positioning</li>
          <li>Versatile tone: from premium to playful</li>
        </ul>
      </AnimatedCardGothic>

      <AnimatedCardGothic
        center
        title="✍️ Want This Level of Copy For Your Brand?"
        delay={1.7}
      >
        <p>
          Whether you're booking charters, selling yachts, or launching a marina
          service — I help you speak to high-end buyers and fill your calendar
          with ease.
        </p>
        <div className="flex justify-center gap-4 mt-4">
          <a
            href="mailto:sadiqboats@gmail.com"
            className="inline-flex items-center justify-center px-4 py-2 bg-red-900 text-gray-200 rounded-md hover:bg-red-800 transition shadow-lg hover:shadow-red-700/80 animate-flame-flicker"
          >
            <Mail className="mr-2 h-4 w-4" /> Email Me
          </a>
          <a
            href="https://www.instagram.com/sadiq.copy?igsh=MWg2N3k4bWtrY3FxNw=="
            target="_blank"
            rel="noopener noreferrer"
            className="inline-flex items-center justify-center px-4 py-2 bg-red-900 text-gray-200 rounded-md hover:bg-red-800 transition shadow-lg hover:shadow-red-700/80 animate-flame-flicker"
          >
            <Instagram className="mr-2 h-4 w-4" /> Instagram
          </a>
        </div>
      </AnimatedCardGothic>
    </div>
  );
}

function AnimatedCardGothic({ title, children, center = false, delay = 0 }) {
  return (
    <motion.div
      initial={{ opacity: 0, y: 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.6, delay }}
      className="mb-6"
    >
      <Card className="border border-gray-700 bg-gray-900 shadow-lg shadow-red-900/30 hover:shadow-red-700/50 transition-shadow rounded-md">
        <CardContent
          className={`p-6 space-y-3 ${center ? "text-center" : ""} text-gray-300`}
          style={{ fontFamily: "'Cinzel', serif" }}
        >
          <h2
            className="text-2xl font-semibold text-red-700 tracking-wide underline decoration-red-800 decoration-2 underline-offset-4 mb-2"
            style={{ fontFamily: "'Cinzel', serif" }}
          >
            {title}
          </h2>
          {children}
        </CardContent>
      </Card>
    </motion.div>
  );
}
