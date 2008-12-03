desc "Copy the vim/doc files into ~/.vim"
task :deploy_local do
  run "cp plugin/NERDSnippets.vim ~/.vim/plugin"
  run "cp doc/NERDSnippets.txt ~/.vim/doc"
end


desc "Create a zip archive for release to vim.org"
task :zip do
  abort "NERDSnippets.zip already exists, aborting" if File.exist?("NERDSnippets.zip")
  run "zip NERDSnippets.zip plugin/NERDSnippets.vim doc/NERDSnippets.txt"
end

def run(cmd)
  puts "Executing: #{cmd}"
  system cmd
end

