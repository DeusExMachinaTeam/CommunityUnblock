<p align="center">
<a href="https://discord.gg/jZHxYdF"><img src="https://user-images.githubusercontent.com/79088546/174318753-aa4f938f-b7a5-49c0-b1cd-fc73b75080f7.png" width="350"/></a>
</p>

# CommunityUnblock

Инструкция помогающая продолжить пользоваться расположенными в Discord и YouTube ресурсами фан сообществ по Ex Machina, находясь в РФ.
Будет по возможности обновляться актуальными способами обхода блокировок.

# Способ обхода блокировок Discord и YouTube от Овера

> **Антивирусы**
>
> *Есть большая вероятность, что антивирусы будут блокировать попытки скачать необходимый нам софт. Поэтому рекомендую их отключить заранее.*

## Устанавливаем Zapret

1. Скачиваем Zapret для Windows с официального репозитория. [<https://github.com/bol-van/zapret>](https://github.com/bol-van/zapret-win-bundle/archive/refs/heads/master.zip)
2. Распаковываем архив в любое место на компьютере.
3. Заходим в папку **zapret-winws**
4. Создаем текстовый файл сразу меняем ему расширение на **cmd** например **fuckrkn.cmd**
5. Вставляем в файл следующие строки и сохраняем.

    ```text
    start "zapret: http,https,quic" /min "%~dp0winws.exe" ^
    --wf-l3=ipv4,ipv6 --wf-tcp=443 --wf-udp=443,50000-65535 ^
    --filter-udp=443 --hostlist="%~dp0list-youtube.txt" --dpi-desync=fake --dpi-desync-repeats=11 --dpi-desync-fake-quic="%~dp0quic_initial_www_google_com.bin" --new ^
    --filter-tcp=443 --hostlist="%~dp0list-youtube.txt" --dpi-desync=fake,split2 --dpi-desync-split-seqovl=1 --dpi-desync-split-tls=sniext --dpi-desync-fake-tls="%~dp0tls_clienthello_www_google_com.bin" --dpi-desync-ttl=4 --new ^
     --filter-udp=443 --hostlist="%~dp0list-discord.txt" --dpi-desync=fake --dpi-desync-udplen-increment=10 --dpi-desync-repeats=6 --dpi-desync-udplen-pattern=0xDEADBEEF --dpi-desync-fake-quic="%~dp0quic_initial_www_google_com.bin" --new ^
    --filter-udp=50000-65535 --dpi-desync=fake,tamper --dpi-desync-any-protocol --dpi-desync-fake-quic="%~dp0quic_initial_www_google_com.bin" --new ^
    --filter-tcp=443 --hostlist="%~dp0list-discord.txt" --dpi-desync=fake,split2 --dpi-desync-autottl=2 --dpi-desync-fooling=md5sig --dpi-desync-fake-tls="%~dp0tls_clienthello_www_google_com.bin"
    ```

6. Создаем в этой же папке файл list-discord.txt и добавляем в него следующие строки.

    ```text
    discord.com
    discord.gg
    discordapp.com
    discordapp.net
    discord.media
    discord-attachments-uploads-prd.storage.googleapis.com
    dis.gd
    discord.co
    discordcdn.com
    discordstatus.com
    ```

7. Теперь запускаем файл **fuckrkn.cmd** с правами администратора. Ютуб и дискорд должны исправно работать. К сожалению вероятность не 100% и возможно конкретно для вашего провайдера потребуется крутить какие то настройки. Для поиска информации я рекомендую посетить форум [ntc.party](https://ntc.party/) если есть VPN, если нет то обсуждение в GitHub запрета <https://github.com/bol-van/zapret/discussions>.

8. Маленькое дополнение, если вы подозреваете что нужный вам сайт блокируется провайдером через ТСПУ, попробуйте добавить его домен в файл **list-youtube.txt** например если добавить туда домен **ntc.party**, то он начнет открываться без VPN.

## Еще пара слов об обходе блокировок

Приведенный мной пример работает именно сейчас и именно на моем провайдере, через неделю, месяц или любой другой промежуток времени всё может измениться. Это значит, что вам рано или поздно потребуется крутить настройки этих программ, но я уверен вы справитесь. Если хочется этого избежать я рекомендую задуматься о приобретении VPN сервиса, вероятнее всего платного сервиса и, что очень важно, не публичного сервиса. С блокировками публичных сервисов нет никаких сложностей уже сейчас. Поэтому я рекомендую объединяйтесь в группы, арендуйте сервера не в РФ и обходите блокировки вместе. Не опускайте руки, помогайте друг другу, вместе мы справимся. Пока мы едины, мы непобедимы!

# Ссылки на некоторые заблокированные ресурсы сообщества

## Discord

* [Discord Deus Ex Machina](https://discord.gg/nq6BsRk)
* [Discord EM2ch](https://discord.gg/AzZQsgDJaD)
* [Discord Павлика RPG](https://discord.gg/6bMzuw793M)

## YouTube

* [Канал Павлика RPG](https://youtube.com/c/rpggameland)
* [Канал EM2ch](https://www.youtube.com/@em2ch)
* [Канал stakan](https://www.youtube.com/@stakanyash)
