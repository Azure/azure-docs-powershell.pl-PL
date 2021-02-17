---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188098"
---
# Get-AzSqlElasticPoolRecommendation

## SYNOPSIS
Otrzymuje elastyczne zalecenia dotyczące puli.

## SKŁADNIA

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSqlElasticPoolRecommendation** otrzymuje elastyczne zalecenia dotyczące puli dla serwera.
Zalecenia te obejmują następujące wartości:
- DatabaseCollection. Zbiór nazw baz danych należących do puli. 
- DatabaseDtuMin. Gwarancja dtu transmisji danych (Data Transmission Unit) dla baz danych w puli elastycznej. 
 -- DatabaseDtuMax. Limit DTU dla baz danych w puli elastycznej. 
- Dtu. DTU gwarantuje elastyczną pulę. 
- StorageMb. Miejsce do magazynowania w megabajtach na elastyczną pulę. 
- Wersja. Wersja na elastyczną pulę. Dopuszczalne wartości dla tego parametru to: Podstawowe, Standardowe i Premium. 
- UwzględnijWszystkieBazyDanych. Wskazuje, czy wszystkie bazy danych w puli elastycznej są zwracane. 
- Nazwa. Nazwa puli elastycznej.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie rekomendacji dotyczących serwera
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

To polecenie otrzymuje elastyczne zalecenia dotyczące puli dla serwera o nazwie Server01.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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
Określa nazwę grupy zasobów, do której jest przypisany serwer.

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

### -ServerName
Określa nazwę serwera, dla którego to polecenie cmdlet otrzymuje zalecenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecom nieujemnaElasticPoolProperties

## NOTATKI

## LINKI POKREWNE
