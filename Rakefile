require 'bundler/setup'
require 'albacore'

desc 'Build it'
build :build do |cmd|
  cmd.sln = 'dot-net/Centroid.sln'
end

desc 'Test it'
test_runner :test => [:build] do |cmd|
  cmd.exe = "dot-net/packages/NUnit.Runners.2.6.3/tools/nunit-console.exe"
  cmd.files = ["dot-net/Centroid.Tests/bin/Debug/Centroid.Tests.dll"]
end

task :default => :build