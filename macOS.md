## Preview not responding

tar czf ~/preview_cache.tgz ~/Library/Containers/com.apple.Preview/ # make a backup copy
rm -rf ~/Library/Containers/com.apple.Preview/

Then, run Preview again, and if the issue is solved, you can remove the backup:

rm ~/preview_cache.tgz
