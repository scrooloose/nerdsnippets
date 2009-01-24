desc "Copy the vim/doc files into ~/.vim"
task :deploy_local do
  run "cp plugin/NERD_snippets.vim ~/.vim/plugin"
  run "cp doc/NERD_snippets.txt ~/.vim/doc"
end


desc "Create a zip archive for release to vim.org"
task :zip do
  abort "NERD_snippets.zip already exists, aborting" if File.exist?("NERD_snippets.zip")
  run "zip NERD_snippets.zip plugin/NERD_snippets.vim doc/NERD_snippets.txt"
end

def run(cmd)
  puts "Executing: #{cmd}"
  system cmd
end

