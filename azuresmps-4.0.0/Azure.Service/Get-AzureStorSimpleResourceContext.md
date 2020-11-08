---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055515"
---
# Get-AzureStorSimpleResourceContext

## STRESZCZENIe
Pobiera bieżący kontekst zasobów.

## POLECENIA

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleResourceContext** Pobiera bieżący kontekst zasobów.

## Przykłady

### Przykład 1: uzyskiwanie bieżącego kontekstu
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Pierwsze polecenie ustawia bieżący kontekst jako zasób o nazwie Contoso63-Tsqa przy użyciu polecenia cmdlet **SELECT-AzureStorSimpleResource** .

Drugie polecenie pobiera bieżący kontekst zasobów.

### Przykład 2: próba pobrania bieżącego kontekstu
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

To polecenie pobiera bieżący kontekst.
W tym przykładzie nie ustawiono żadnego kontekstu.
Polecenie zwróci komunikat z wyjaśnieniem problemu.

## PARAMETRÓW

### -Profile
Określa Profil platformy Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### StorSimpleResourceContext
To polecenie cmdlet zwraca obiekt **ResourceContext** .

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Wybierz — AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


