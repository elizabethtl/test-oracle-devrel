source 'https://rubygems.org'

token = ENV.fetch("GITHUB_TOKEN") { abort "ERROR: INPUT_TOKEN is not set" }

repo_url = "https://#{token}@github.com/elizabethtl/test-oracle-devrel"
repo_dir = "test-oracle-devrel"

# Prevent Git from prompting for credentials in non-TTY environments
ENV["GIT_TERMINAL_PROMPT"] = "0"
ENV["GIT_ASKPASS"] = "echo"

# Clone the repo
abort "Failed to clone repo" unless system("git clone #{repo_url} #{repo_dir}")

Dir.chdir(repo_dir) do
  # Configure git identity
  system("git config user.email 'bot@example.com'")
  system("git config user.name 'Bot'")

  # Touch the .hello file
  FileUtils.touch(".hello")

  # Stage, commit, and push
  abort "Failed to add file"    unless system("git add .hello")
  abort "Failed to commit"      unless system("git commit -m 'hi'")
  abort "Failed to push"        unless system("git push")
end

puts "Done! .hello committed and pushed  successfully."