task :default => :build

task :build do
  sh "jekyll"
end

task :deploy => :build do
  target = "kacprzak@galaxy.agh.edu.pl:~/public_html"
  source = "_site/*"

  sh <<CMD
scp -r #{source} #{target}
CMD
end
