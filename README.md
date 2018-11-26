A simple program to print data as Go byte slices.

Why? Because I couldn't figure out how to do this with `hexdump` or `xxd`, and
the last 3 times I spent far too long parsing the `hexdump` output with Vim
macros/substitution patterns.

Usage example (output elided):

	$ go get github.com/teamwork/asbyte
	$ asbyte a.*
	// nolint: lll
	var (
		a_gif = []byte{0x47, 0x49, 0x46, 0x38, ...}
		a_jpeg = []byte{0xff, 0xd8, 0xff, 0xe0, ...}
		a_png = []byte{0x89, 0x50, 0x4e, 0x47, 0xd, ...}
	)
