# Sadiqimport { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Anchor, Star } from "lucide-react";

export default function YachtCopywritingPortfolio() {
  return (
    <div className="max-w-4xl mx-auto p-6 space-y-6">
      <h1 className="text-4xl font-bold text-center">🚤 Yacht & Boating Copywriting Portfolio</h1>
      <p className="text-center text-lg text-muted-foreground">By Sadiq [Your Last Name] – Luxury & Lifestyle Copywriter</p>
      <p className="text-center italic">"I help yacht brands turn cold leads into booked-out seasons — using storytelling, sales psychology, and high-end copywriting."</p>

      <Card>
        <CardContent className="p-4 space-y-2">
          <h2 className="text-2xl font-semibold">🎯 Client Niche</h2>
          <p>Yacht Charters · Boat Builders · Marine Luxury Brands · Marina Services</p>
        </CardContent>
      </Card>

      <Card>
        <CardContent className="p-4 space-y-4">
          <h2 className="text-2xl font-semibold">📬 Email Sequence Overview</h2>
          <p><strong>Campaign Theme:</strong> "The SailSmart Productivity System – A Lead Nurture Funnel for Yacht Business Owners"</p>
          <ul className="list-disc list-inside">
            <li>Turn disengaged leads into paying clients</li>
            <li>Revive underperforming offers</li>
            <li>Launch or scale a premium course or service</li>
            <li>Position the brand as luxury, emotional, and in-demand</li>
          </ul>
        </CardContent>
      </Card>

      {[
        {
          title: "Email 1: The Intriguing Origin Story",
          sl: "I nearly sold the whole fleet.",
          highlight: "Emotional storytelling + transformation arc"
        },
        {
          title: "Email 2: Unique Mechanism Email",
          sl: "The shift that saved my charter business",
          highlight: "Introduces proprietary method + clear logic for change"
        },
        {
          title: "Email 3: Value With Sass & Personality",
          sl: "That 'Marketing Guru' never owned a yacht",
          highlight: "Voice-driven, fun, anti-fluff copy"
        },
        {
          title: "Email 4: Subtle Frustration Hook",
          sl: "Why are you still stuck in the harbor, {{name}}?",
          highlight: "Uses frustration to spark action"
        },
        {
          title: "Email 5: Logic + Empathy Email",
          sl: "Stop wasting time on offers no one wants",
          highlight: "High-ticket clarity without hustle"
        },
        {
          title: "Email 6: Sales Page Primer",
          sl: "One wrong click rewired Sal’s yacht business",
          highlight: "Case study storytelling + deep transformation"
        },
        {
          title: "Email 7: Urgency Closer",
          sl: "Spots are sailing fast. Are you on board?",
          highlight: "Bold CTA and urgency framing"
        }
      ].map((email, index) => (
        <Card key={index}>
          <CardContent className="p-4 space-y-2">
            <h3 className="text-xl font-semibold">{email.title}</h3>
            <p><strong>Subject Line:</strong> {email.sl}</p>
            <p><strong>Highlight:</strong> {email.highlight}</p>
          </CardContent>
        </Card>
      ))}

      <Card>
        <CardContent className="p-4 space-y-2">
          <h2 className="text-2xl font-semibold">🛟 Writing Features Showcased</h2>
          <ul className="list-disc list-inside">
            <li>High-converting storytelling</li>
            <li>Emotional connection & clarity</li>
            <li>Nautical/luxury brand vocabulary</li>
            <li>Strategic offer positioning</li>
            <li>Versatile tone: from premium to playful</li>
          </ul>
        </CardContent>
      </Card>

      <Card>
        <CardContent className="p-4 space-y-4 text-center">
          <h2 className="text-2xl font-semibold">✍️ Want This Level of Copy For Your Brand?</h2>
          <p>Whether you're booking charters, selling yachts, or launching a marina service — I help you speak to high-end buyers and fill your calendar with ease.</p>
          <Button className="mt-2" variant="default">
            <Mail className="mr-2 h-4 w-4" /> Contact Me
          </Button>
        </CardContent>
      </Card>
    </div>
  );
}
