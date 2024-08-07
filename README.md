# A-Gravity-s-Rainbow-Hypergraph
# About
"We have to look for power sources here, and distribution networks we were never taught, routes of power our teachers never imagined, or were encouraged to avoid ... we have to find meters whose scales are unknown in the world, draw our own schematics, getting feedback, making connections, reducing the error, trying to learn the real function ... zeroing in on what incalculable plot?" (521). 
<br />

Gravity's Rainbow, in both style and substance, is a novel about human attempts to impose order on and construct meaning from the torrent of sensory data that floods our senses at every moment. Pavlovianism, statistics, rocketry, organic chemistry, Kabbalah, Rosicrucianism, Protestantism, Tarot, Astrology, military industrial conspiracies, S&M and more are all depicted as methods of systematizing and constructing meaning out of a stream of information that may be nothing more than noise. Pynchon digs into the technical minutiae of these methods, exposing their common structure and shared origin as an expression of human longing for meaning. Or, as per [Richard Poirier](https://gravitys-rainbow.pynchonwiki.com/wiki/index.php?title=Rocket_Power) "It is not enough to say that Pynchon records the effects of technology on human lives or adapts the methods of technology to the investigation and dramatization of them ... He is locating the  kinds of human consciousness that have been implanted <i>in</i> the instruments of technology and contemporary methods of analysis; not content with recording the historical effect of these, he is anxious  to find our history <i>in</i> them." The plot mirrors these themes, bombarding the reader with an endless succession of characters, plots, agencies, connections and conspiracies that overwhelm the working memory. We become like Slothrop, that peripatetic paranoid, searching for hidden connections, signs of election, something to latch onto. It sure beats the alternative: "If there is something comforting - religous, if you want - about paranoia, there is still also anti-paranoia, where nothing is connected to anything, a condition not many of us can bear for long" (434).<br/>


# The Math
"If tensor analysis is good enough for turbulence, it ought to be good enough for history. There ought to be nodes, critical points ... 
there ought to be super-derivatives of the crowded and insatiate flow that can be set equal to zero and those critical points found" (451).  

With these ideas in mind, I set out to turn modern mathematical methods of analysis on the novel itself and attempt to impose my own order on its apparent chaos. I began by asking the most basic, structural question: who are the characters and how are they connected? The most intuitive way to structure such information is with a graph. A graph is defined as a set of nodes (in this case characters) and connections (pairs of nodes). However, because Gravity's Rainbow is about not only the connections of individual characters, but the interactions between groups of characters that comprise organizations, I knew that a graph, which is limited only to pairwise connections between nodes, would not suffice to capture all of the relevant information. Formally, what you are looking at is a hypergraph, defined as H = (X,E) where X is the set of nodes (e.g. X = {Tyrone Slothrop, Roger Mexico, Katje Borgesius,...}) and E is a set of non-empty subsets of X, known as hyperedges, which encapsulate both standard pairwise connections e.g. {Vaslav Tchitcherine, Geli Tripping}, represented as an a line between nodes, but also groups of arbitrary size such as the Argentinian Anarchists: {Francisco Squalidozzi, Luz, Felipe, El Nato, Belaustegui, Graciela Imago Portales}, represented by rectangles around nodes. Similar efforts had already been made for the <a href = ""> [major characters/ideas](https://sciencekings.com/GravitysRainbowCharacters.pdf) of Gravity's Rainbow, the characters of [Inherent Vice](https://inherent-vice.com/) and for other novels with many characters such as [Les Mis](https://colab.research.google.com/github/pnnl/HyperNetX/blob/master/tutorials/Tutorial%203%20-%20LesMis%20Case%20Study.ipynb), but I wanted to make something that 1) included every character in one network, 2) adhered more closely to what I thought was the natural graph structure of characters as nodes, edges as connections, groups as hyperedges and 3) could be open sourced into an interactive, wiki like project that others could benefit from and contribute to.  


# Methodology
"If you want the truth - I know I presume - you must look into the technology of these matters. Even into the hearts of
certain molecules - it is they after all which dictate temperatures, pressures, rates of flow, costs, profits, the shapes
of towers" (167).  

This network was first drawn by hand while reading (which I recommend avoiding doing in a public space past maybe 10 characters), then input to the computer graphically using [Cytoscape](https://cytoscape.org/), and displayed using [Cytoscape.js](https://js.cytoscape.org) with html. Obtaining a useable layout with a minimal number of edge crossings was [hard](https://en.wikipedia.org/wiki/Crossing_number_(graph_theory)#Complexity_and_approximation) but after messing around with algorithmic formatting I settled on a hand drawn layout. Nodes can be clicked and dragged to make for easier reading. Certain important groups such as The Counterforce are omitted as their membership crosses multiple group boundaries, making it difficult to draw cleanly. I am working on other methods of visualizing these hyperedges. 

My criteria for including a character was that the character is 1) named and 2) performs some action in the context of the novel. This criteria excludes individuals such as Richard Nixon, who is named but does not perform any action, as well as the dancers and chimpanzees of GMB Haftung, who perform actions, but remain unnamed.  Using this criteria I ended up with 242 characters which is well below the 400 quoted in secondary sources, which likely count historical figures as well as unnamed characters. 

All page numbers referenced here and in the graph are from the 1995 Penguin Twentieth Century Classics edition of Gravity's Rainbow (with the blue rocket diagram on the cover), which is coneveniently the same as [this](http://books.google.com/books?id=iPDGp7VT8H8C&printsec=frontcover) searchable Google Books copy. Those with access to Weisenburger's companion could probably translate roughly between editions.


# Planned improvements and ideas for contributions
"Of course a well-developed They-system is necessary - but it's only half the story. For every They there ought to be a We. In our case there is.
Creative paranoia means developing at least as thorough a We-system as a They-system ... We don't have to worry about questions of real or unreal
... It's the <i>system</i> that matters. How the data arrange themselves inside it. Some are consistent, others fall apart" (638).

This project is open source and in theory anyone with ideas for improvements should feel free to submit a pull request.

Planned improvements:
- General style fixes
- Using index of characters by order of appearance to allow for the generation of spoiler free networks up to the end of books 1, 2, 3 and 4.
- Upgrade to allow for direct, graphical editing or the network for users who are not familiar with coding/git. 

Ideas for contributions:
- Enhanced edge information, including page number references.
- Clarification of the membership of the hyperedges SHAEF, SPOG, Operation Blackwing as well as the various subgroups of Hereros.
- Characters indexed by order of appearance to page level accuracy to allow for the generation of spoiler free networks up to exact pages.
- Enhanced node/character information available on clicking/hovering.
- Searchable nodes/hyperedges 
