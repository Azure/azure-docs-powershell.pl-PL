---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542392"
---
# Get-AzureRmRedisCacheLink

## STRESZCZENIe
Uzyskaj link replikacji Geo dla pamięci podręcznej Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### AllLinksForCache (domyślny)
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Istnieją cztery różne sposoby uzyskiwania szczegółów linku replikacji geograficznej. Podaj nazwę parametru lub PrimaryServerName i/lub SecondaryServerName. Imię i nazwisko, a wszystkie linki, w których istnieje pamięć podręczna, zostaną zwrócone. Jeśli jest podany tylko PrimaryServerName, zostaną zwrócone wszystkie linki, w przypadku których pamięć podręczna jest podstawowa. Jeśli jest podany tylko SecondaryServerName, zostaną zwrócone wszystkie linki, w których pamięć podręczna jest pomocnicza. Jeśli PrimaryServerName i SecondaryServerName są podane, zostanie zwrócona konkretna wartość linku o odpowiedniej roli. 

## Przykłady

### Przykład 1: uzyskiwanie używania zestawu parametrów AllLinksForCache
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

To polecenie pobiera wszystkie linki replikacji geograficznej dla pamięci podręcznej Redis o nazwie mycache1.

### Przykład 2: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForPrimaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache1 to Primary.

### Przykład 3: uzyskiwanie dostępu za pomocą zestawu parametrów AllLinksForSecondaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

To polecenie pobiera linki replikacji geograficznej, w której Redis pamięć podręczna o nazwie mycache2 jest pomocnicza.

### Przykład 4: uzyskiwanie używania zestawu parametrów SingleLink
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

To polecenie pobiera pojedyncze linki replikacji geograficznej, w której pamięć podręczna Redis o nazwie mycache1 jest podstawowa, a pamięć podręczna Redis o nazwie mycache2 jest pomocnicza.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa pamięci podręcznej Redis.

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Nazwa pamięci podręcznej Redis głównej w łączu.

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Nazwa pomocniczej pamięci podręcznej Redis w łączu.

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String
Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. RedisCache. MODELES. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmRedisCacheLink](./New-AzureRmRedisCacheLink.md)

[Remove-AzureRmRedisCacheLink](./Remove-AzureRmRedisCacheLink.md)

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Nowe — AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)
