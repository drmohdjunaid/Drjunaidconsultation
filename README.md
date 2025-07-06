# Drjunaidconsultation
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Mail, Phone, Clock, Stethoscope, MessageSquare } from "lucide-react";
import Link from "next/link";

export default function Home() {
  return (
    <div className="max-w-5xl mx-auto px-4 py-8">
      <h1 className="text-4xl font-bold text-center mb-4">
        Online Medical Consultation Services
      </h1>
      <p className="text-center text-lg mb-8">
        Consult with <strong>Dr. Mohd Junaid</strong> <br />
        General Physician & Emergency Medicine
      </p>

      <section className="grid grid-cols-1 md:grid-cols-2 gap-4">
        <Card>
          <CardContent className="p-4">
            <h2 className="text-2xl font-semibold mb-2">About Dr. Junaid</h2>
            <p><strong>Qualifications:</strong> BAMS, PGDEMS</p>
            <p><strong>Specialization:</strong> Emergency Medicine & General Diseases</p>
          </CardContent>
        </Card>

        <Card>
          <CardContent className="p-4">
            <h2 className="text-2xl font-semibold mb-2">Consultation Details</h2>
            <p><Clock className="inline mr-2" /> Available: 9:00 AM - 9:00 PM</p>
            <p><Stethoscope className="inline mr-2" /> Mode: Online (WhatsApp / Video)</p>
            <p><MessageSquare className="inline mr-2" /> Languages: English, Hindi, Urdu</p>
          </CardContent>
        </Card>

        <Card className="md:col-span-2">
          <CardContent className="p-4">
            <h2 className="text-2xl font-semibold mb-2">Contact & Booking</h2>
            <p><Phone className="inline mr-2" /> <a href="tel:+919876543210">+91 98765 43210</a></p>
            <p><Mail className="inline mr-2" /> <a href="mailto:drjunaid@example.com">drjunaid@example.com</a></p>

            <div className="mt-4 flex flex-col md:flex-row gap-4">
              <Link href="https://wa.me/919876543210" target="_blank">
                <Button className="w-full md:w-auto bg-green-600 hover:bg-green-700">
                  Chat on WhatsApp
                </Button>
              </Link>

              <Link href="https://calendly.com/drjunaid/consultation" target="_blank">
                <Button className="w-full md:w-auto">
                  Schedule Now
                </Button>
              </Link>
            </div>
          </CardContent>
        </Card>
      </section>
    </div>
  );
}
