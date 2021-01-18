---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498962"
---
# Get-AzMediaServiceKey

## STRESZCZENIe
Pobiera kluczowe informacje dotyczące uzyskiwania dostępu do punktu końcowego usługi w usłudze multimediów skojarzonego z usługą Media.

## POLECENIA

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzMediaServiceKey** pobiera informacje kluczowe o uzyskiwaniu dostępu do punktu końcowego przenoszenia stanu (pozostałej) skojarzonego z usługą Azure Media.

## Przykłady

### Przykład 1: uzyskiwanie najważniejszych informacji dotyczących uzyskiwania dostępu do usługi multimedialnej
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

To polecenie pobiera kluczowe informacje dotyczące uzyskiwania dostępu do usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup001.

## PARAMETRÓW

### -AccountName
Określa nazwę usługi multimedialnej, z której to polecenie cmdlet pobiera klucze usługi multimedialnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej usługę Media.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Media. models. PSServiceKeys

## INFORMACYJN

## LINKI POKREWNE

[Set-AzMediaServiceKey](./Set-AzMediaServiceKey.md)


