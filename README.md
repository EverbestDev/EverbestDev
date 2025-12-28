<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-50 to-white">
    <!-- Back Button -->
    <div class="fixed top-6 left-6 z-50">
      <router-link
        to="/"
        class="flex items-center gap-2 text-[#2e8b57] hover:text-[#246d43] font-semibold transition-all hover:gap-3 bg-white/80 backdrop-blur-sm px-4 py-2 rounded-lg shadow-md hover:shadow-lg"
      >
        <ArrowLeft :size="20" />
        <span>Back to Home</span>
      </router-link>
    </div>

    <!-- Header -->
    <div class="relative bg-gradient-to-r from-[#2e8b57] to-[#246d43] text-white py-20 overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 40px 40px;"></div>
      </div>
      
      <div class="relative container mx-auto max-w-4xl px-6 text-center">
        <div class="flex justify-center mb-6">
          <div class="w-20 h-20 rounded-full bg-white/10 backdrop-blur-sm flex items-center justify-center border-2 border-white/30 shadow-2xl">
            <Cookie :size="40" class="text-white" />
          </div>
        </div>
        <h1 class="text-4xl md:text-5xl font-bold mb-4">Cookie Policy</h1>
        <p class="text-lg text-white/90">Last updated: {{ currentDate }}</p>
      </div>
    </div>

    <!-- Content -->
    <div class="container mx-auto max-w-4xl px-6 py-16">
      <div class="bg-white rounded-2xl shadow-xl p-8 md:p-12 border border-gray-100">
        
        <!-- Introduction -->
        <div class="mb-12 p-6 bg-gradient-to-r from-[#2e8b57]/5 to-[#246d43]/5 rounded-xl border-l-4 border-[#2e8b57]">
          <p class="text-gray-700 leading-relaxed text-lg">
            At E-Attendance, we believe in transparency and your right to privacy. This Cookie Policy explains what cookies are, how we use them, and the choices you have regarding their use. We are committed to protecting your personal information and your right to privacy.
          </p>
        </div>

        <!-- What Are Cookies -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <Info :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">What Are Cookies</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-4">
            Cookies are small text files that are placed on your device (computer, smartphone, or tablet) when you visit a website. They are widely used to make websites work more efficiently and provide a better user experience. Cookies allow websites to recognize your device and remember information about your visit, such as your preferred language and other settings.
          </p>
          <p class="text-gray-600 leading-relaxed">
            These files contain small amounts of data and are stored in your web browser. They help us understand how you interact with our service, remember your preferences, and improve your overall experience with E-Attendance.
          </p>
        </section>

        <!-- How We Use Cookies -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <CheckCircle2 :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">How We Use Cookies</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-6">
            When you use and access E-Attendance, we may place a number of cookie files in your web browser. We use cookies for the following purposes to enhance your experience and improve our service:
          </p>
          <div class="space-y-4">
            <div class="group p-6 bg-gradient-to-br from-white to-gray-50 rounded-xl border border-gray-200 hover:border-[#2e8b57]/30 hover:shadow-lg transition-all duration-300">
              <div class="flex items-start gap-4">
                <div class="p-3 bg-[#2e8b57]/10 rounded-lg group-hover:bg-[#2e8b57]/20 transition-colors">
                  <Lock :size="24" class="text-[#2e8b57]" />
                </div>
                <div class="flex-1">
                  <h3 class="font-bold text-gray-800 text-lg mb-2">Essential Cookies</h3>
                  <p class="text-gray-600 mb-3">These cookies are strictly necessary for the operation of our service. They enable core functionality such as security, network management, and accessibility.</p>
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Authentication</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Security</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Session Management</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="group p-6 bg-gradient-to-br from-white to-gray-50 rounded-xl border border-gray-200 hover:border-[#2e8b57]/30 hover:shadow-lg transition-all duration-300">
              <div class="flex items-start gap-4">
                <div class="p-3 bg-[#2e8b57]/10 rounded-lg group-hover:bg-[#2e8b57]/20 transition-colors">
                  <BarChart3 :size="24" class="text-[#2e8b57]" />
                </div>
                <div class="flex-1">
                  <h3 class="font-bold text-gray-800 text-lg mb-2">Analytics & Performance Cookies</h3>
                  <p class="text-gray-600 mb-3">These cookies help us understand how visitors interact with our service by collecting and reporting information anonymously. This helps us improve the functionality and user experience.</p>
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Usage Analytics</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Performance Monitoring</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Error Tracking</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="group p-6 bg-gradient-to-br from-white to-gray-50 rounded-xl border border-gray-200 hover:border-[#2e8b57]/30 hover:shadow-lg transition-all duration-300">
              <div class="flex items-start gap-4">
                <div class="p-3 bg-[#2e8b57]/10 rounded-lg group-hover:bg-[#2e8b57]/20 transition-colors">
                  <Settings2 :size="24" class="text-[#2e8b57]" />
                </div>
                <div class="flex-1">
                  <h3 class="font-bold text-gray-800 text-lg mb-2">Functional & Preference Cookies</h3>
                  <p class="text-gray-600 mb-3">These cookies enable the service to provide enhanced functionality and personalization. They remember your preferences and choices to provide a more personalized experience.</p>
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Language Settings</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">Theme Preferences</span>
                    <span class="px-3 py-1 bg-[#2e8b57]/10 text-[#2e8b57] text-xs rounded-full font-medium">User Preferences</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>

        <!-- Third-Party Cookies -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <Shield :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Third-Party Cookies</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-4">
            In addition to our own cookies, we may also use various third-party cookies to report usage statistics of the service and deliver advertisements on and through the service. These third-party services have their own privacy policies addressing how they use such information.
          </p>
          <div class="bg-amber-50 border-l-4 border-amber-400 p-6 rounded-lg">
            <div class="flex items-start gap-3">
              <AlertCircle :size="20" class="text-amber-600 mt-0.5 flex-shrink-0" />
              <div>
                <p class="font-semibold text-amber-900 mb-2">Important Note</p>
                <p class="text-amber-800 text-sm leading-relaxed">
                  We do not have access to or control over third-party cookies. We encourage you to review the privacy policies of these third-party services for more information about their practices.
                </p>
              </div>
            </div>
          </div>
        </section>

        <!-- Cookie Duration -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <Clock :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Cookie Duration</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-6">
            Different cookies have different lifespans. Understanding cookie duration helps you make informed decisions about your privacy:
          </p>
          <div class="grid md:grid-cols-2 gap-6">
            <div class="group p-6 bg-gradient-to-br from-blue-50 to-blue-100/50 rounded-xl border border-blue-200 hover:shadow-lg transition-all">
              <div class="flex items-center gap-3 mb-3">
                <div class="relative w-16 h-16 rounded-lg overflow-hidden bg-blue-500 flex items-center justify-center group-hover:scale-110 transition-transform">
                  <img src="https://images.unsplash.com/photo-1614064641938-3bbee52942c7?w=400&h=400&fit=crop" alt="Session Cookies" class="w-full h-full object-cover opacity-20" />
                  <Zap :size="24" class="text-white absolute" />
                </div>
                <h3 class="font-bold text-gray-800 text-lg">Session Cookies</h3>
              </div>
              <p class="text-gray-600 text-sm leading-relaxed">
                Temporary cookies that are deleted when you close your browser. They help maintain your session while navigating through our service.
              </p>
            </div>
            <div class="group p-6 bg-gradient-to-br from-purple-50 to-purple-100/50 rounded-xl border border-purple-200 hover:shadow-lg transition-all">
              <div class="flex items-center gap-3 mb-3">
                <div class="relative w-16 h-16 rounded-lg overflow-hidden bg-purple-500 flex items-center justify-center group-hover:scale-110 transition-transform">
                  <img src="https://images.unsplash.com/photo-1506784365847-bbad939e9335?w=400&h=400&fit=crop" alt="Persistent Cookies" class="w-full h-full object-cover opacity-20" />
                  <Calendar :size="24" class="text-white absolute" />
                </div>
                <h3 class="font-bold text-gray-800 text-lg">Persistent Cookies</h3>
              </div>
              <p class="text-gray-600 text-sm leading-relaxed">
                Remain on your device for a set period or until you delete them. They remember your preferences and settings for future visits.
              </p>
            </div>
          </div>
        </section>

        <!-- Managing Cookie Preferences -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <Settings :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Managing Your Cookie Preferences</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-6">
            You have the right to decide whether to accept or reject cookies. You can exercise your cookie rights by setting your preferences in your browser settings. Most web browsers are set to accept cookies by default, but you can adjust your browser settings to remove or reject cookies if you prefer.
          </p>
          
          <div class="bg-gradient-to-br from-[#2e8b57]/5 to-[#246d43]/5 rounded-xl p-6 mb-6 border border-[#2e8b57]/20">
            <h3 class="font-bold text-gray-800 mb-4 flex items-center gap-2">
              <Globe :size="20" class="text-[#2e8b57]" />
              Browser-Specific Instructions
            </h3>
            <div class="grid md:grid-cols-2 gap-4">
              <a href="https://support.google.com/chrome/answer/95647" target="_blank" class="flex items-center justify-between p-4 bg-white rounded-lg hover:shadow-md transition-shadow group">
                <span class="text-gray-700 font-medium">Google Chrome</span>
                <ExternalLink :size="16" class="text-gray-400 group-hover:text-[#2e8b57]" />
              </a>
              <a href="https://support.mozilla.org/en-US/kb/enhanced-tracking-protection-firefox-desktop" target="_blank" class="flex items-center justify-between p-4 bg-white rounded-lg hover:shadow-md transition-shadow group">
                <span class="text-gray-700 font-medium">Mozilla Firefox</span>
                <ExternalLink :size="16" class="text-gray-400 group-hover:text-[#2e8b57]" />
              </a>
              <a href="https://support.apple.com/guide/safari/manage-cookies-sfri11471/mac" target="_blank" class="flex items-center justify-between p-4 bg-white rounded-lg hover:shadow-md transition-shadow group">
                <span class="text-gray-700 font-medium">Safari</span>
                <ExternalLink :size="16" class="text-gray-400 group-hover:text-[#2e8b57]" />
              </a>
              <a href="https://support.microsoft.com/en-us/microsoft-edge/delete-cookies-in-microsoft-edge-63947406-40ac-c3b8-57b9-2a946a29ae09" target="_blank" class="flex items-center justify-between p-4 bg-white rounded-lg hover:shadow-md transition-shadow group">
                <span class="text-gray-700 font-medium">Microsoft Edge</span>
                <ExternalLink :size="16" class="text-gray-400 group-hover:text-[#2e8b57]" />
              </a>
            </div>
          </div>

          <div class="bg-red-50 border-l-4 border-red-400 p-6 rounded-lg">
            <div class="flex items-start gap-3">
              <AlertTriangle :size="20" class="text-red-600 mt-0.5 flex-shrink-0" />
              <div>
                <p class="font-semibold text-red-900 mb-2">Important Considerations</p>
                <p class="text-red-800 text-sm leading-relaxed mb-2">
                  Please note that if you delete cookies or refuse to accept them, you might not be able to use all of the features we offer. Specifically, you may experience:
                </p>
                <ul class="text-red-800 text-sm space-y-1 ml-4 list-disc">
                  <li>Difficulty staying logged in to your account</li>
                  <li>Loss of personalized settings and preferences</li>
                  <li>Reduced functionality on certain pages</li>
                  <li>Need to re-enter information more frequently</li>
                </ul>
              </div>
            </div>
          </div>
        </section>

        <!-- Updates to Policy -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <FileText :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Updates to This Cookie Policy</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-4">
            We may update our Cookie Policy from time to time to reflect changes in our practices or for other operational, legal, or regulatory reasons. When we make significant changes, we will notify you by:
          </p>
          <div class="space-y-3">
            <div class="flex items-start gap-3 p-4 bg-gray-50 rounded-lg">
              <CheckCircle2 :size="20" class="text-[#2e8b57] flex-shrink-0 mt-0.5" />
              <p class="text-gray-600">Updating the "Last updated" date at the top of this Cookie Policy</p>
            </div>
            <div class="flex items-start gap-3 p-4 bg-gray-50 rounded-lg">
              <CheckCircle2 :size="20" class="text-[#2e8b57] flex-shrink-0 mt-0.5" />
              <p class="text-gray-600">Posting a notice on our homepage or within the application</p>
            </div>
            <div class="flex items-start gap-3 p-4 bg-gray-50 rounded-lg">
              <CheckCircle2 :size="20" class="text-[#2e8b57] flex-shrink-0 mt-0.5" />
              <p class="text-gray-600">Sending an email notification if you have provided your email address</p>
            </div>
          </div>
          <p class="text-gray-600 leading-relaxed mt-4">
            We encourage you to periodically review this Cookie Policy to stay informed about how we are using cookies and protecting your information.
          </p>
        </section>

        <!-- FAQ Section -->
        <section class="mb-10">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <HelpCircle :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Frequently Asked Questions</h2>
          </div>
          <div class="space-y-4">
            <details class="group bg-white border border-gray-200 rounded-lg overflow-hidden hover:border-[#2e8b57]/30 transition-colors">
              <summary class="flex items-center justify-between p-6 cursor-pointer font-semibold text-gray-800 hover:text-[#2e8b57] transition-colors">
                <span>Do I have to accept cookies to use E-Attendance?</span>
                <ChevronDown :size="20" class="text-gray-400 group-open:rotate-180 transition-transform" />
              </summary>
              <div class="px-6 pb-6 text-gray-600 leading-relaxed border-t border-gray-100 pt-4">
                Essential cookies are required for the basic functionality of our service. However, you can choose to opt-out of non-essential cookies such as analytics and preference cookies. Please note that disabling certain cookies may limit your experience on our platform.
              </div>
            </details>

            <details class="group bg-white border border-gray-200 rounded-lg overflow-hidden hover:border-[#2e8b57]/30 transition-colors">
              <summary class="flex items-center justify-between p-6 cursor-pointer font-semibold text-gray-800 hover:text-[#2e8b57] transition-colors">
                <span>How long do cookies stay on my device?</span>
                <ChevronDown :size="20" class="text-gray-400 group-open:rotate-180 transition-transform" />
              </summary>
              <div class="px-6 pb-6 text-gray-600 leading-relaxed border-t border-gray-100 pt-4">
                The duration varies depending on the type of cookie. Session cookies are deleted when you close your browser, while persistent cookies remain on your device for a predetermined period (ranging from days to years) or until you manually delete them.
              </div>
            </details>

            <details class="group bg-white border border-gray-200 rounded-lg overflow-hidden hover:border-[#2e8b57]/30 transition-colors">
              <summary class="flex items-center justify-between p-6 cursor-pointer font-semibold text-gray-800 hover:text-[#2e8b57] transition-colors">
                <span>Can cookies contain viruses or malware?</span>
                <ChevronDown :size="20" class="text-gray-400 group-open:rotate-180 transition-transform" />
              </summary>
              <div class="px-6 pb-6 text-gray-600 leading-relaxed border-t border-gray-100 pt-4">
                No, cookies are simple text files and cannot contain viruses or execute programs. They cannot install malware on your device or access your hard drive. However, they can be used to track your browsing behavior across websites.
              </div>
            </details>

            <details class="group bg-white border border-gray-200 rounded-lg overflow-hidden hover:border-[#2e8b57]/30 transition-colors">
              <summary class="flex items-center justify-between p-6 cursor-pointer font-semibold text-gray-800 hover:text-[#2e8b57] transition-colors">
                <span>Will deleting cookies affect my saved data on E-Attendance?</span>
                <ChevronDown :size="20" class="text-gray-400 group-open:rotate-180 transition-transform" />
              </summary>
              <div class="px-6 pb-6 text-gray-600 leading-relaxed border-t border-gray-100 pt-4">
                No, your account data and attendance records are securely stored on our servers and are not affected by cookie deletion. However, you may need to log in again and re-configure your preferences after deleting cookies.
              </div>
            </details>
          </div>
        </section>

        <!-- Contact Section -->
        <section>
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-full bg-[#2e8b57]/10 flex items-center justify-center">
              <Mail :size="20" class="text-[#2e8b57]" />
            </div>
            <h2 class="text-2xl font-bold text-gray-800">Contact Us</h2>
          </div>
          <p class="text-gray-600 leading-relaxed mb-6">
            If you have any questions, concerns, or requests regarding our Cookie Policy or how we handle cookies, we're here to help. Our support team is committed to addressing your privacy concerns promptly and transparently.
          </p>
          <div class="bg-gradient-to-br from-[#2e8b57]/10 to-[#246d43]/10 rounded-xl p-8 border border-[#2e8b57]/30">
            <div class="grid md:grid-cols-2 gap-6">
              <div class="flex items-start gap-4">
                <div class="p-3 bg-white rounded-lg shadow-sm">
                  <Mail :size="24" class="text-[#2e8b57]" />
                </div>
                <div>
                  <p class="font-semibold text-gray-800 mb-1">Email Support</p>
                  <a href="mailto:support@eattendance.com" class="text-[#2e8b57] hover:text-[#246d43] transition-colors font-medium">
                    support@eattendance.com
                  </a>
                  <p class="text-sm text-gray-600 mt-1">Response within 24-48 hours</p>
                </div>
              </div>
              
              <div class="flex items-start gap-4">
                <div class="p-3 bg-white rounded-lg shadow-sm">
                  <MessageCircle :size="24" class="text-[#2e8b57]" />
                </div>
                <div>
                  <p class="font-semibold text-gray-800 mb-1">Live Chat</p>
                  <p class="text-gray-600">Available Monday - Friday</p>
                  <p class="text-sm text-gray-600 mt-1">9:00 AM - 6:00 PM (WAT)</p>
                </div>
              </div>
            </div>
            
            <div class="mt-6 pt-6 border-t border-[#2e8b57]/20">
              <p class="text-sm text-gray-600 leading-relaxed">
                <strong class="text-gray-800">Data Protection Officer:</strong> For specific privacy and data protection inquiries, you can reach our Data Protection Officer at 
                <a href="mailto:dpo@eattendance.com" class="text-[#2e8b57] hover:text-[#246d43] transition-colors font-medium"> dpo@eattendance.com</a>
              </p>
            </div>
          </div>
        </section>

        <!-- Footer Note -->
        <div class="mt-12 pt-8 border-t border-gray-200">
          <div class="bg-gray-50 rounded-xl p-6 text-center">
            <div class="flex justify-center mb-3">
              <div class="p-3 bg-white rounded-full shadow-sm">
                <Shield :size="24" class="text-[#2e8b57]" />
              </div>
            </div>
            <p class="text-gray-600 text-sm leading-relaxed max-w-2xl mx-auto">
              Your privacy matters to us. This Cookie Policy is part of our commitment to transparency and protecting your personal information. 
              For more details about how we protect your data, please review our 
              <router-link to="/privacy-policy" class="text-[#2e8b57] hover:text-[#246d43] font-semibold transition-colors">Privacy Policy</router-link> and 
              <router-link to="/terms-of-service" class="text-[#2e8b57] hover:text-[#246d43] font-semibold transition-colors">Terms of Service</router-link>.
            </p>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import { 
  ArrowLeft, 
  Cookie, 
  Info, 
  Lock, 
  BarChart3, 
  Settings2, 
  Settings,
  Mail,
  CheckCircle2,
  Shield,
  AlertCircle,
  Clock,
  Zap,
  Calendar,
  Globe,
  ExternalLink,
  AlertTriangle,
  FileText,
  HelpCircle,
  ChevronDown,
  MessageCircle
} from "lucide-vue-next";

const currentDate = computed(() => {
  return new Date().toLocaleDateString('en-US', { 
    year: 'numeric', 
    month: 'long', 
    day: 'numeric' 
  });
});
</script>

<style scoped>
section {
  scroll-margin-top: 2rem;
}

details summary::-webkit-details-marker {
  display: none;
}

details[open] summary {
  margin-bottom: 0;
}
</style>
