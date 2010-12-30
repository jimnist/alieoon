##
# tasks for maintaining and deploying this site
#
# adapted and simplified from:
#    http://davidwparker.com/2009/12/01/my-jekyll-rake-file/
#
# relies on public key being set up for the user on the host

SSH_ALIAS = "jimnist"
SITE_NAME = "alieoon.org"

desc "deploy #{SITE_NAME} to dreamhost"
task :deploy do
  puts "building site"
  system('compass')
  puts "rsynching.."  
  system("rsync -avrz site/ #{SSH_ALIAS}:#{SITE_NAME}/public")
end

desc "run thin and compass dev servers"
task :dev do
  system "./scripts/dev_servers.sh"
end
