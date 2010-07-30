Quickly install with:

    git clone git://github.com/msanders/snipmate.vim.git
	cd snipmate.vim
	cp -R * ~/.vim




find . -type d -and -not -iwholename '*git*' -and -not -iwholename '*READ*' -and -iwholename '*snip*' -exec echo \{} \;| perl -e 'my $pwd = $ENV{PWD};my @data = <>; chomp @data; map { s/\.//; print "ln -s $pwd$_ $ENV{HOME}/.vim$_\n" } @data;' | sh

find . -type f -and -not -iwholename '*git*' -and -not -iwholename '*READ*' -exec echo \{} \; |\
 perl -e 'my $pwd = $ENV{PWD};my @data = <>; chomp @data; map { s/\.//; print "ln -s $pwd$_ $ENV{HOME}/.vim$_\n" } @data;' | sh
