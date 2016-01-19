clean:
	rm -rf public

serve: clean
	hugo server -t markup --watch

publish: clean
	hugo -t markup
	rsync -e "ssh -p 22" -P -rvz --delete public/*  thatmattbone@thatmattbone.com:/home/thatmattbone/opensource.thatmattbone.com

# used to have:
# --include .htaccess
