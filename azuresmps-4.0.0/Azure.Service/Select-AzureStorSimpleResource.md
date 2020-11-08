---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054414"
---
# Select-AzureStorSimpleResource

## STRESZCZENIe
Ustawia zasób jako bieżący zasób.

## POLECENIA

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **SELECT-AzureStorSimpleResource** ustawia zasób jako bieżący zasób.
Po wybraniu zasobu inne polecenia cmdlet będą stosowane w tym kontekście zasobów.

## Przykłady

### Przykład 1. Wybieranie zasobu po raz pierwszy
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

To polecenie umożliwia wybranie zasobu o nazwie Contoso64-Tsqa jako bieżącego kontekstu.
W tym przykładzie nie zainicjowano wcześniej tego kontekstu na komputerze, dlatego należy określić wartość parametru *RegistrationKey* .

### Przykład 2: próba wybrania zasobu
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### Przykład 3: Zaznaczanie uprzednio wybranego zasobu
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

To polecenie umożliwia wybranie zasobu o nazwie Contoso64-Tsqa jako bieżącego kontekstu.
W tym przykładzie kontekst został już wybrany, a więc nie musisz określać wartości parametru *RegistrationKey* .

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

### -RegistrationKey
Określa klucz rejestracji.
Określ klucz przy pierwszym wybraniu zasobu.
Gdy to polecenie cmdlet wybierzesz bieżący zasób, polecenia cmdlet użyją tego klucza stosownie do potrzeb.
Aby uzyskać więcej informacji, zobacz [Uzyskiwanie klucza rejestracji usługi](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) w witrynie Microsoft Developer Network.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Określa nazwę zasobu, który ma zostać wybrany jako bieżący zasób.

```yaml
Type: String
Parameter Sets: (All)
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

### Znaleziono

## WYSYŁA

### StorSimpleResourceContext
To polecenie cmdlet zwraca obiekt **StorSimpleResourceContext** , który zawiera szczegółowe informacje dotyczące kontekstu zasobów.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


