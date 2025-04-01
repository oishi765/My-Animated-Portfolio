# My-Animated-Portfolio
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { FaGithub, FaLinkedin, FaFacebook } from "react-icons/fa";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-900 text-white flex flex-col items-center p-6">
      <motion.h1 
        className="text-4xl font-bold text-center mt-10"
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        👋 Hi, I'm Evana Hossain Oishi!
      </motion.h1>
      
      <motion.p 
        className="text-lg text-gray-300 mt-4 text-center max-w-2xl"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1 }}
      >
        🚀 Aspiring Cybersecurity Specialist | 💻 Undergraduate ICT Student at BUP
      </motion.p>
      
      <div className="grid md:grid-cols-2 gap-6 mt-10">
        <Card className="bg-gray-800 p-4 rounded-2xl shadow-lg">
          <CardContent>
            <h2 className="text-xl font-semibold mb-2">📌 About Me</h2>
            <p className="text-gray-300">Currently learning computer fundamentals, networking, and C++. Passionate about cybersecurity, ethical hacking, and system security.</p>
          </CardContent>
        </Card>

        <Card className="bg-gray-800 p-4 rounded-2xl shadow-lg">
          <CardContent>
            <h2 className="text-xl font-semibold mb-2">🎯 2025 Goals</h2>
            <ul className="list-disc pl-4 text-gray-300">
              <li>Learn Python</li>
              <li>Master Data Structures & Algorithms</li>
              <li>Explore Cryptography</li>
              <li>Participate in CTF Competitions</li>
              <li>Gain hands-on experience in cybersecurity tools</li>
            </ul>
          </CardContent>
        </Card>
      </div>

      <motion.div 
        className="flex space-x-4 mt-10"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1.2 }}
      >
        <Button asChild variant="outline" className="text-white">
          <a href="https://github.com" target="_blank"><FaGithub size={24} /></a>
        </Button>
        <Button asChild variant="outline" className="text-white">
          <a href="https://www.linkedin.com/in/evana-hossain-oishi-8988512b4" target="_blank"><FaLinkedin size={24} /></a>
        </Button>
        <Button asChild variant="outline" className="text-white">
          <a href="https://www.facebook.com/profile.php?id=100025626674232" target="_blank"><FaFacebook size={24} /></a>
        </Button>
      </motion.div>
    </div>
  );
}
