# Rollin9-Blocks
Blockchain Application Idea Submission | codefundo++

Problem Statement ー 
We plan to implement a secure voters’ list. It must ensure automatic addition of names for people crossing the age of 18 and that no eligible voter is left out of the voters’ list due to manipulation by a malicious party.

Assumptions taken include ー
Accurate and genuine list of names provided to the Election Commission (possibly through the Aadhar dataset).
Election Commission centres will only delete names if person is actually dead (e.g. they are provided a death certificate).
Election Commision will also handle change of name or change of constituency and it is upon them to verify legitimacy of such a claim.

Planning to build ー
Blockchain implementation of voter’s list
Automatic addition of names on turning 18 (automatic only for a person having Aadhar, else it is manual)

How does it work?
Only the Election Commission’s Regional Offices should be able to add data (i.e. write to a block) to the blockchain. Hence we’ll implement a private blockchain. A list of people exists (say via Aadhar) including constituency details. We maintain a list of eligible voters using a token based system. Whenever a person turns 18 he/she automatically gets a token allotted to them. This token stays with their name(UID that is used internally) until they die, so this blockchain is maintained yearlong regardless of elections. We also provide for change of name and change of constituency. If you own an Aadhar card if you change any of these two details, we generate a new UID for the updated data, and give the new ID a token. We remove the token from the old ID thus preventing misuse via two voter entries for the same person. If a person dies the token is taken back. All of these transactions can only be done by an election office. 
We also propose to use Aadhar for convenience of those who have Aadhar  (Aadhar can’t be  compulsory as per SC) . If any details are changed in the Aadhar account as far as name or constituency are concerned out system will automatically update using the token system as described above. 
On the day of election each voting booth can ensure they are receiving correct voters list by verifying the block chain hash values for manipulation. We also propose creating a system for a member of the public to verify that Polling Booth heads don’t locally hide names despite having the correct list by giving interested members of the public a key/hash value online or something so they can independently verify.
 
How users can get started with the project?
Our users here are the Election Commission regional offices, each of which will have to maintain a node on our blockchain. We’ll provide an interface for them to change data on the blockchain.

For citizens, If you have an Aadhar you don’t need to do anything. Else you’ll have to approach Election Commission's representatives with all the requisite proof. This is a one time trip and you’ll only need to visit them again in case of name/constituency change.

Dataset(s): Dummy Aadhar dataset

Technologies: Microsoft Azure Blockchain (Hyperledger), git, Github, Docker, Go language, Microsoft VSCode, HTML, CSS
