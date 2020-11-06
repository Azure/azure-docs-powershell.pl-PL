---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542835"
---
# Get-AzureRmSqlElasticPoolRecommendation

## STRESZCZENIe
Pobiera elastyczne rekomendacje.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmSqlElasticPoolRecommendation** umożliwia pobieranie elastycznych rekomendacji dla serwera.
Zalecenia te obejmują następujące wartości:

- DatabaseCollection. Kolekcja nazw baz danych należących do puli. 
- DatabaseDtuMin. Gwarancja jednostki transmisji danych (DTU) dla baz danych w puli elastycznej. 
 -- DatabaseDtuMax. WPR (DTU Cap) dla baz danych w puli elastycznej. 
- DTU. Gwarancja jednostek DTU dla puli elastycznej. 
- StorageMb. Miejsce do magazynowania w megabajtach dla puli elastycznej. 
- Edition. Wersja dla puli elastycznej. Dopuszczalne wartości tego parametru to: Basic, standard i Premium. 
- IncludeAllDatabases. Wskazuje, czy zostaną zwrócone wszystkie bazy danych w puli elastycznej. 
- Nazwę. Nazwa puli elastycznej.

## Przykłady

### Przykład 1: uzyskiwanie rekomendacji dla serwera
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

To polecenie uzyskuje rekomendacje dotyczące puli elastycznej dla serwera o nazwie Server01.

## PARAMETRÓW

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

### -Nazwa_serwera
Określa nazwę serwera, dla którego jest pobierana rekomendacja tego polecenia cmdlet.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

