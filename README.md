\\\\
RU
\\\\

это комплекс решений для обеспечения безопастности 
конфиденциальной информации. оно переводит в другую 
форму или код, так только люди имеюзие
 доступ к 
секретному ключу или паролю, могут прочитать его.

например ассиметричное шифрование, когда это 
комплекс решений для обеспечения безопастности 
конфиденциальной информации. оно переводит в другую 
форму или код, так только люди имеюзие доступ к 
секретному ключу или паролю, могут прочитать его. 
например чтобы клиенты могли общаться в чате , 
перекидывать сообщения только по своим публичным 
ключам:
 клиент1 - например шифрует свое сообщение публичным 
 ключем клиента2. Оно отправляется на сервер, сервер 
 все это дело зашифровывает и расшифровать может 
 только тот для кого это сообщение должно было дойти 
 своим приватным ключем
То есть мы можем сгенерировать ключ , создаем 
приватные файлы, которые не передаем, клиенты могут 
обмениваться файлами помимо сервера, можем их 
шифровать но и расшифровать может только клиент1 или 
клиент2, сам наш получатель. расшифровываем 
сообщенте из публичного ключа, который идет через 
сервер, своим приватным ключем, который есть у 
получателя.  то есть асимметричное шифрование — это 
сам  метод, использующий пару ключей (публичный и 
приватный), чтобы обеспечить безопасность передачи 
данных в мессенджерах, VPN, HTTPS.это частный случай 
data encryption.одна из техник data encryption.
Представьте волшебный почтовый ящик и он имеет замок 
с двумя ключами.Один ключ публичный – его можно 
раздавать всем,  тем с кем вы общаетесь и кто 
захочет тебе отправлять сообщения и переписываться с 
тобой.
Другой ключ приватный  и  он есть только у тебя, и 
его нельзя никому ни показывать ни говорить  и им 
можно открывать замок.В итоге, как это работает:

Человек, который хочет отправить тебе послание, 
кладёт его в ящик и закрывает на твой публичный ключ.
И теперь никто, даже отправитель, не может открыть 
ящик – потому что открыть его можно только приватным 
ключом, который есть у тебя.я получаю коробку, 
использую свой приватный ключ и читаю сообщение.

и  преимущество в том, что даже если кто-то 
перехватит коробку, он не сможет её открыть!
но как приватный ключ может открыть то, что было 
зашифровано публичным ключом.
Главное правило асимметричного шифрования:
 То, что зашифровано публичным ключом, может быть 
 расшифровано только соответствующим приватным 
 ключом и наоборот.

Потому что пара ключей {публичный -**- приватный} 
математически связаны друг с другом, но мы не можем  
вычислить приватный ключ по публичному. Это 
достигается за счёт математических алгоритмов,
например RSA (это разложение больших чисел на 
множители),ECC (эллиптические кривые), 
Diffie-Hellman (используется для обмена ключами)
Когда данные шифруются публичным ключом, они 
изменяются так, что их можно расшифровать только с 
помощью "парного" приватного ключа.
ы итоге асимметричное шифрование — это метод, 
обеспечивающий безопасность передачи данных, VPN, 
HTTPS и особенно в мессенджерах(например в Telegram 
в секретных чатах ). Оно переводит данные в 
зашифрованную форму, используя пару ключей — 
публичный (public key) и приватный (private key).

Итог:
Клиент1 шифрует сообщение публичным ключом Клиента2.
Сообщение отправляется на сервер в зашифрованном 
виде.
Сервер не может его расшифровать, потому что не 
владеет приватным ключом.
Клиент2 получает сообщение и расшифровывает его 
своим приватным ключом.
То есть даже если злоумышленник перехватит данные на 
сервере или в сети, он не сможет их прочитать без 
приватного ключа получателя.

Генерация ключей: создаються приватные файлы 
(например, .pem, .key), которые никогда не 
передаются по сети, а публичные ключи можно свободно 
распространять.
Обмен файлами напрямую между клиентами (минуя 
сервер), но в зашифрованном виде, расшифровать их 
сможет только получатель.

Цифровая подпись — это способ проверить подлинность 
данных. эот  доказательство, что данные 
действительно отправлены конкретным человеком и не 
были изменены.При обычном шифровании публичный ключ 
шифрует, а приватный расшифровывает.В цифровой 
подписи всё наоборот: приватный ключ так сказать 
"подписывает", а публичный ключ проверяет.если мы 
хотим отправить важный документ например, договор, и 
доказать, что он действительно от тебя.
мне нужно создать цифровую подпись..я беру свой 
документ и вычисляю его хеш с помощью алгоритма 
SHA-256.

и я шифрую этот хеш своим приватным ключом. Это и 
есть цифровая подпись. потом я отправляю документ 
вместе с подписью, получатель проверяет подпись и он 
тоже должен вычислить хеш документа. он берёт мою 
цифровую подпись и расшифровывает её публичным 
ключом.

Если расшифрованный хеш совпадает с вычисленным – 
значит, документ действительно от мееня и его никто 
не подделал!

Подделать подпись нельзя – ведь только у меня есть 
приватный ключ.Любой может проверить подлинность – 
потому что твой публичный ключ доступен всем,если 
кто-то изменит хоть 1 символ в документе, хеш 
изменится, и подпись окажется недействительной.
цифровая подпись мспользуеться в SSL/
TLS-сертификатах (HTTPS) – сайты подписывают свои 
данные, и браузеры проверяют их подлинность,к 
риптовалюты (Bitcoin, Ethereum) – каждая транзакция 
подписывается приватным ключом отправителя 
Электронные документы () юридически значимые файлы) .
цифровая подпись не шифрует данные а только 
подтверждает что тот документ подлинный и он не 
изменился



плюс в  HTTPS асимметричное шифрование используется 
только для обмена ключами, а затем трафик 
переключается на симметричное шифрование, потому что 
оно быстрее.  \\Forward Secrecy (протоколы TLS) 
создаются временные ключи для каждой сессии,и  если 
один ключ будет скомпрометирован, нельзя бедут 
расшифровать старые сообщения.
\\В криптографии часто используют эллиптические 
кривые (\\ECC), потому что они дают такую же защиту, 
как RSA, но с гораздо меньшими размерами ключей и 
вычислительной нагрузкой.

Генерируются два ключа (публичный e,n и приватный d,
n)

Шифровка:
Отправитель берёт текст сообщения (например, 
"Hello") и превращает его в число (M).
Затем возводит M в степень e (из публичного ключа) 
по модулю n:

𝐶=𝑀(" в степени) mod 𝑛
число C – это зашифрованное сообщение.
Получатель берёт C и возводит его в степень d (из 
приватного ключа) по модулю n:
𝑀=𝐶(𝑑 в степени) mod 𝑛
M=C(𝑑 в степени) mod n
В результате получается исходное сообщение M.

Алгоритм RSA устроен так, что зашифровать можно 
публичным ключом, но расшифровать только приватным – 
потому что e и d связаны математически, но найти d 
зная e практически невозможно из-за сложности 
разложения больших чисел на множители.

\\\\
EN
\\\\
This is a set of solutions to ensure the security of 
confidential information. It converts data into 
another form or code so that only people with access 
to a secret key or password can read it.

For example, asymmetric encryption is when this set 
of solutions ensures the security of confidential 
information. It converts data into another form or 
code so that only people with access to a secret key 
or password can read it.

For instance, so that clients can communicate in a 
chat and exchange messages only using their public 
keys:
Client1, for example, encrypts their message with 
the public key of Client2. It is sent to the server, 
the server keeps everything encrypted, and only the 
intended recipient can decrypt it with their private 
key.

That means we can generate a key, create private 
files that we do not share, and clients can exchange 
files outside the server. We can encrypt them, but 
only Client1 or Client2—our recipient—can decrypt 
them. We decrypt the message, which was sent using 
the public key through the server, with the private 
key that the recipient possesses.

So, asymmetric encryption is a method that uses a 
pair of keys (public and private) to ensure secure 
data transmission in messengers, VPNs, and HTTPS. It 
is a specific case of data encryption—one of its 
techniques.

Imagine a magical mailbox that has a lock with two 
keys.
One key is public—it can be given to everyone you 
communicate with and anyone who wants to send you 
messages.
The other key is private—it belongs only to you, and 
you must never show or share it. It is used to 
unlock the lock.

Here’s how it works:
1️ A person who wants to send you a message puts it 
in the mailbox and locks it with your public key.
2️ Now no one, not even the sender, can open the 
mailbox—because it can only be opened with the 
private key that only you have.

 You receive the box, use your private key, and read 
 the message.

The advantage is that even if someone intercepts the 
box, they won’t be able to open it!

But how can a private key unlock something that was 
encrypted with a public key?

The main rule of asymmetric encryption:
What is encrypted with a public key can only be 
decrypted with its corresponding private key—and 
vice versa.

This works because the key pair {public -**- 
private} is mathematically linked, but you cannot 
derive the private key from the public one. This is 
achieved through mathematical algorithms such as:

RSA (Rivest-Shamir-Adleman) – based on the 
factorization of large numbers
ECC (Elliptic Curve Cryptography) – uses elliptic 
curves for stronger security with smaller key sizes
Diffie-Hellman – used for secure key exchange
When data is encrypted with a public key, it is 
transformed in such a way that it can only be 
decrypted using the "paired" private key.

So, asymmetric encryption is a method ensuring 
secure data transmission, used in VPNs, HTTPS, and 
especially messengers (for example, Telegram secret 
chats). It converts data into an encrypted format 
using a pair of keys—public and private.

Process:
Client1 encrypts a message with Client2’s public key.
The message is sent to the server in encrypted form.
The server cannot decrypt it because it does not 
have the private key.
Client2 receives the message and decrypts it with 
their private key.
This means that even if an attacker intercepts the 
data on the server or network, they cannot read it 
without the recipient’s private key.


Key Generation:
Private files (e.g., .pem, .key) are created but 
never transmitted over the network.
Public keys can be freely shared.
Files can be exchanged directly between clients 
(bypassing the server) in encrypted form, and only 
the recipient can decrypt them.
Digital Signature – Verifying Data Authenticity
A digital signature is a way to verify the 
authenticity of data. It is proof that data was 
actually sent by a specific person and was not 
altered.



In normal encryption, the public key encrypts and 
the private key decrypts.

In digital signatures, it’s the opposite:

The private key "signs"

The public key verifies
For example, if I want to send an important document 
(like a contract) and prove that it’s really from me:



I create a digital signature by:

Taking my document and computing its hash using 
SHA-256 (a hashing algorithm that converts data into 
a fixed-length string).
Encrypting this hash with my private key—this 
becomes my digital signature.

I send the document along with the signature.



 The recipient verifies the signature:

They compute the document’s hash.They decrypt my 
digital signature using my public key.
If the decrypted hash matches the computed one → the 
document is authentic and was not altered.
Why is this secure?
Forgery is impossible – only I have my private key.
Anyone can verify authenticity – because my public 
key is available.
If even 1 character in the document changes, the 
signature becomes invalid!
Where Digital Signatures Are Used?
SSL/TLS certificates (HTTPS) – Websites sign their 
data, and browsers verify their authenticity.
Cryptocurrencies (Bitcoin, Ethereum) – Each 
transaction is signed with the sender’s private key.

Electronic documents (legal contracts, secure 
emails).
A digital signature does not encrypt data but 
confirms that a document is authentic and has not 
been modified.


In HTTPS, asymmetric encryption is used only for key 
exchange.

After that, the traffic switches to symmetric 
encryption, which is faster.
Perfect Forward Secrecy (TLS protocols)
Temporary keys are created for each session.
If one key is compromised, old messages cannot be 
decrypted.
Elliptic Curve Cryptography (ECC)
ECC provides the same level of security as RSA but 
with smaller key sizes and less computational power.
How RSA Encryption Works:

Two keys are generated:
Public key (e, n)
Private key (d, n)


The sender converts the message into a number M (e.
g., "Hello" → M).
They compute:
C = M^e mod n (encrypted message).

The receiver takes C and computes:
M = C^d mod n (original message).
Why is RSA Secure?
You can encrypt with the public key, but only the 
private key can decrypt.
e and d are mathematically linked, but finding d 
from e is practically impossible due to the 
difficulty of factoring large numbers.

This ensures security in modern communications, from 
HTTPS and VPNs to encrypted messengers and 
blockchain transactions
