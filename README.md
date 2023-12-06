# goot-research
Research into the Goot

Each phase will be numbered. The file contents are B64 encoded.

Key takeaways:
1. The PS script will poll environment values, concatenate them with the "^" character.
2. The PS script will beacon to one of the ten domains at random.
3. The cookie will be set to include each B64 encoded ENV values.
4. The first cookie value will be used to parse the XML RPC response from the C2 server.
5. The value at index 1 will be executed via the PS Invoke-Expression cmdlet.

Need to get PCAP showing the response... Possibly sample that PS-Script in a sandbox and try modifying stuff to see the responses.

Maybe:
Execute the ENV polling commands on a real PC (at home, non-attributable, or at a friend's house lol), concat with "^", and B64 encode. Download new Goot in Sandbox with the NIC emulated. Manually modify the ENV calls with the B64 values. Execute the script to let it beacon out.
