---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: d360a468d69306b5f203cbd28d17e9bfcc00bdcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526894"
---
# New-AzureRmDataFactoryGatewayKey

## STRESZCZENIe
Tworzy klucz bramy dla fabryki danych platformy Azure. To polecenie cmdlet jest przestarzałe i zamiast tego powinno być używane polecenie **New-AzureRmDataFactoryGatewayAuthKey** .

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByFactoryName (domyślny)
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmDataFactoryGatewayKey** tworzy klucz bramy dla określonej bramy usługi Azure Data Factory.
Użytkownik rejestruje bramę w usłudze chmury za pomocą tego klucza. To polecenie cmdlet jest przestarzałe i zamiast tego powinno być używane polecenie **New-AzureRmDataFactoryGatewayAuthKey** .

## Przykłady

### Przykład 1. Tworzenie klucza bramy
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

To polecenie tworzy klucz bramy dla bramy fabryki danych o nazwie ContosoGateway, a następnie przekazuje klucz bramy do polecenia cmdlet Format-List przy użyciu operatora potoku.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .

## PARAMETRÓW

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet tworzy klucz bramy dla fabryki danych, którą określa ten parametr.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Określa nazwę fabryki danych.
To polecenie cmdlet tworzy klucz bramy dla fabryki danych, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Bramaname
Określa nazwę bramy.
To polecenie cmdlet tworzy klucz dla bramy, którą ten parametr określa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet tworzy klucz dla bramy należącej do grupy, którą ten parametr określa.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Nowe — AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Nowe — AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)


