require 'rubygems'
require 'bundler/setup'

require 'asciidoctor'
require 'rake/clean'

CLEAN.include 'output/'

task :default => :build

desc "Build the doc"
task :build do
  Dir.mkdir 'output' unless File.directory? 'output'
  system "bundle exec asciidoctor --safe-mode unsafe -a copycss -a toc -D output Book.asciidoc"
end

