import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";

export default function EventikaHome() {
  return (
    <main className="bg-black text-white min-h-screen p-4 font-sans graffiti-bg">
      <nav className="flex justify-between items-center py-4 px-6 bg-black/80 backdrop-blur-md sticky top-0 z-50 border-b border-pink-600">
        <div className="text-2xl font-bold graffiti-style">Eventika.rw</div>
        <div className="space-x-4">
          <Button variant="ghost" className="text-white hover:text-pink-400">Home</Button>
          <Button variant="ghost" className="text-white hover:text-pink-400">Events</Button>
          <Button variant="ghost" className="text-white hover:text-pink-400">Artists</Button>
          <Button variant="ghost" className="text-white hover:text-pink-400">Contact</Button>
        </div>
      </nav>

      <header className="text-center py-10">
        <h1 className="text-4xl md:text-6xl font-bold graffiti-style">
          Lights On. Sound Up. Let's Go!
        </h1>
        <p className="mt-4 text-lg md:text-xl">
          Discover the hottest events in Rwanda — music, culture, nightlife & more
        </p>
      </header>

      <section className="grid md:grid-cols-3 gap-4 p-4">
        {[1, 2, 3].map((i) => (
          <Card key={i} className="bg-gray-900/80 text-white rounded-2xl shadow-xl border border-pink-500">
            <CardContent className="p-4">
              <h2 className="text-2xl font-semibold mb-2 graffiti-style">Event Title {i}</h2>
              <p className="text-sm text-gray-300">
                Short description of this amazing event. Date, time, location.
              </p>
              <Button className="mt-4 bg-pink-600 hover:bg-pink-500">Learn More</Button>
            </CardContent>
          </Card>
        ))}
      </section>

      <section className="bg-gray-800/90 rounded-2xl p-6 mt-10 max-w-3xl mx-auto border border-purple-500">
        <h2 className="text-2xl font-bold mb-4 graffiti-style">Submit Your Event</h2>
        <form className="space-y-4">
          <Input placeholder="Event Name" className="bg-gray-700 border-none text-white" />
          <Input placeholder="Date & Time" className="bg-gray-700 border-none text-white" />
          <Input placeholder="Location" className="bg-gray-700 border-none text-white" />
          <Textarea placeholder="Event Description" className="bg-gray-700 border-none text-white" />
          <Button type="submit" className="bg-pink-600 hover:bg-pink-500">Submit Event</Button>
        </form>
      </section>

      <section className="bg-gray-900/90 rounded-2xl p-6 mt-10 max-w-3xl mx-auto border border-yellow-400">
        <h2 className="text-2xl font-bold mb-4 graffiti-style">Artist Sign-Up</h2>
        <form className="space-y-4">
          <Input placeholder="Artist Name" className="bg-gray-700 border-none text-white" />
          <Input placeholder="Genre" className="bg-gray-700 border-none text-white" />
          <Input placeholder="Contact Email" className="bg-gray-700 border-none text-white" />
          <Textarea placeholder="Bio / Description" className="bg-gray-700 border-none text-white" />
          <Button type="submit" className="bg-yellow-500 hover:bg-yellow-400 text-black">Sign Up</Button>
        </form>
      </section>

      <section className="bg-gray-800/90 rounded-2xl p-6 mt-10 max-w-3xl mx-auto border border-cyan-400">
        <h2 className="text-2xl font-bold mb-4 graffiti-style">Contact Us</h2>
        <form className="space-y-4">
          <Input placeholder="Your Name" className="bg-gray-700 border-none text-white" />
          <Input placeholder="Your Email" className="bg-gray-700 border-none text-white" />
          <Textarea placeholder="Your Message" className="bg-gray-700 border-none text-white" />
          <Button type="submit" className="bg-cyan-500 hover:bg-cyan-400 text-black">Send Message</Button>
        </form>
      </section>

      <footer className="text-center text-gray-400 mt-10 text-sm">
        &copy; {new Date().getFullYear()} Eventika.rw — All rights reserved
      </footer>

      <style jsx>{`
        .graffiti-bg {
          background-image: url('/nunu.jpg');
          background-size: cover;
          background-position: center;
          background-repeat: no-repeat;
        }
        .graffiti-style {
          font-family: 'Bangers', cursive;
          color: #ff2e63;
          text-shadow: 2px 2px #000;
        }
      `}</style>
    </main>
  );
}
