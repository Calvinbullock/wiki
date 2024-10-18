# Ubuntu core dumps

## set core dump patter
`sudo sysctl -w kernel.core_pattern=core.%p.%s.%c.%d.%P`

## core dump size
`ulimit -c 8`
