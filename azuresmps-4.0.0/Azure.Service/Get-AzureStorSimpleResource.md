---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054520"
---
# Get-AzureStorSimpleResource

## STRESZCZENIe
Pobiera wszystkie utworzone przez siebie zasoby.

## POLECENIA

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleResource** umożliwia pobieranie wszystkich zasobów utworzonych za pomocą portalu Azure Portal.
Polecenie cmdlet umożliwia pobieranie szczegółów, których można użyć w celu nawiązania połączenia z zasobami.

## Przykłady

### Przykład 1: pobieranie wszystkich zasobów
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

To polecenie umożliwia pobieranie wszystkich utworzonych zasobów.
W tym przykładzie występują trzy zasoby.

### Przykład 2: Pobieranie zasobu przy użyciu jego nazwy
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

To polecenie uzyskuje zasób o nazwie Contoso63-Tsqa.

### Przykład 3: próba uzyskania nieistniejącego zasobu
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

To polecenie próbuje uzyskać zasób o nazwie Contoso64-Tsqa.
Brak zasobu o tej nazwie.
W tym przykładzie nie są zwracane żadne zasoby.

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

### -ResourceName
Określa nazwę zasobu, który jest pobierany przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### Interfejs IEnumerable \<ResourceCredentials\> , ResourceCredentials
To polecenie cmdlet zwraca obiekty **ResourceCredentials** zawierające następujące właściwości: 

- **Source**
- **ResouceId**
- **ResourceState**

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[Wybierz — AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


