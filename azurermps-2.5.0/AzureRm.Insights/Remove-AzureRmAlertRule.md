---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: b0fc044ee2a4704c9bb6803ab0cf7a4be4ea95e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898473"
---
# <span data-ttu-id="c9166-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9166-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="c9166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9166-102">SYNOPSIS</span></span>
<span data-ttu-id="c9166-103">Usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="c9166-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9166-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9166-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9166-105">DESCRIPTION</span></span>
<span data-ttu-id="c9166-106">Polecenie cmdlet **Remove-AzureRmAlertRule** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c9166-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="c9166-107">Musisz określić nazwę reguły alertu i grupę zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="c9166-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="c9166-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9166-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c9166-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9166-109">EXAMPLES</span></span>

### <span data-ttu-id="c9166-110">Przykład 1: Usuwanie reguły alertu</span><span class="sxs-lookup"><span data-stu-id="c9166-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="c9166-111">To polecenie usuwa regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8 w grupie zasobów domyślne — Centrala internetowa.</span><span class="sxs-lookup"><span data-stu-id="c9166-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="c9166-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9166-112">PARAMETERS</span></span>

### <span data-ttu-id="c9166-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9166-113">-DefaultProfile</span></span>
<span data-ttu-id="c9166-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9166-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9166-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9166-115">-Name</span></span>
<span data-ttu-id="c9166-116">Określa nazwę reguły alertu, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="c9166-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9166-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9166-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9166-118">Określa nazwę grupy zasobów dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c9166-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9166-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9166-119">-Confirm</span></span>
<span data-ttu-id="c9166-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9166-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9166-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9166-121">-WhatIf</span></span>
<span data-ttu-id="c9166-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9166-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9166-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9166-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9166-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9166-124">CommonParameters</span></span>
<span data-ttu-id="c9166-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9166-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9166-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9166-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9166-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9166-127">INPUTS</span></span>

### <span data-ttu-id="c9166-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c9166-128">System.String</span></span>

## <span data-ttu-id="c9166-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9166-129">OUTPUTS</span></span>

### <span data-ttu-id="c9166-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c9166-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c9166-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9166-131">NOTES</span></span>

## <span data-ttu-id="c9166-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9166-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9166-133">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9166-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c9166-134">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9166-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c9166-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c9166-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c9166-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9166-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


