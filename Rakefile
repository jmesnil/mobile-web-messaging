require 'rubygems'
require 'bundler/setup'

require 'asciidoctor'
require 'rake/clean'

CLEAN.include 'output/'

task :default => :build

desc "Build the doc"
task :build do
  Dir.mkdir 'output' unless File.directory? 'output'
  system "bundle exec asciidoctor --safe-mode unsafe -a copycss -a toc2 -a toc.section.depth=3 -D output Book.asciidoc"
end

desc "Build the draft outline"
task :outline do
  Dir.mkdir 'output' unless File.directory? 'output'
  system "bundle exec asciidoctor --safe-mode unsafe -a copycss -a toc2 -D output Working-Outline.asciidoc"
end