---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542315"
---
# Install-AzureRmServerManagementGatewayProfile

## STRESZCZENIe
Instaluje profil bramy zarządzania serwera.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Install-AzureRmServerManagementGatewayProfile** instaluje profil bramy usługi Azure Server Management Gateway w odpowiedniej lokalizacji.
Plik, który jest instalowany przez to polecenie cmdlet, nosi nazwę profile.jswłączony.

## Przykłady

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

### -Plik_wejściowy
Określa nazwę pliku lokalnego zawierającego profil bramy do zainstalowania.

Plik, który jest instalowany przez to polecenie cmdlet, powinien być wcześniej zapisany za pomocą polecenia cmdlet Save-AzureRmServerManagementGatewayProfile.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### FileInfo
Parametr "plik_wejściowy" przyjmuje wartość typu "FileInfo" z rurociągu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Resetowanie — AzureRmServerManagementGatewayProfile](./Reset-AzureRmServerManagementGatewayProfile.md)

[Zapisz — AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


