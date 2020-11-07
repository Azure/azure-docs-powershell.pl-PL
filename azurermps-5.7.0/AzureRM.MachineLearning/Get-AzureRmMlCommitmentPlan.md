---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718914"
---
# Get-AzureRmMlCommitmentPlan

## STRESZCZENIe
Pobiera informacje podsumowujące dla co najmniej jednego planu zobowiązań.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Pobiera informacje dotyczące planu zobowiązań.
W zależności od przekazanego paramenters polecenie cmdlet zwraca określony plan zobowiązań, kolekcję planów zobowiązań dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję planów zobowiązań w ramach bieżącej subskrypcji.

## Przykłady

### --------------------------Przykład 1: uzyskiwanie określonego planu zobowiązań--------------------------
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### --------------------------Przykład 2: pobieranie wszystkich zasobów planu zobowiązań w bieżącej subskrypcji--------------------------
```
Get-AzureRmMlCommitmentPlan
```

### --------------------------Przykład 3: Pobierz wszystkie plany zobowiązań w bieżącym abonamentu i danej grupie zasobów--------------------------
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## PARAMETRÓW

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

### -Name (nazwa)
Nazwa planu zobowiązań.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.

```yaml
Type: String
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
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan
Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure

## LINKI POKREWNE

