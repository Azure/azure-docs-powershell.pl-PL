---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896861"
---
# <span data-ttu-id="e7b51-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7b51-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e7b51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7b51-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b51-103">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="e7b51-103">Removes a workspace.</span></span>

## <span data-ttu-id="e7b51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7b51-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7b51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7b51-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b51-106">Polecenie cmdlet **Remove-AzOperationalInsightsWorkspace** usuwa istniejący obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="e7b51-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="e7b51-107">Jeśli ten obszar roboczy był połączony z istniejącym kontem za pośrednictwem parametru *IDKlienta* w czasie tworzenia, oryginalne konto nie zostanie usunięte w portalu usługi Insights.</span><span class="sxs-lookup"><span data-stu-id="e7b51-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="e7b51-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7b51-108">EXAMPLES</span></span>

### <span data-ttu-id="e7b51-109">Przykład 1. Usuń obszar roboczy według nazwy</span><span class="sxs-lookup"><span data-stu-id="e7b51-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="e7b51-110">To polecenie usuwa obszar roboczy o nazwie Moja przestrzeń robocza z grupy zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e7b51-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e7b51-111">Przykład 2: Usuwanie obszaru roboczego za pomocą potoku i bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="e7b51-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="e7b51-112">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Remove-AzOperationalInsightsWorkspace** przy użyciu operatora potoku w celu usunięcia go.</span><span class="sxs-lookup"><span data-stu-id="e7b51-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="e7b51-113">Ponieważ parametr *Force* jest określony, polecenie nie wyświetla monitu przed usunięciem obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e7b51-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="e7b51-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7b51-114">PARAMETERS</span></span>

### <span data-ttu-id="e7b51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b51-115">-DefaultProfile</span></span>
<span data-ttu-id="e7b51-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e7b51-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b51-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e7b51-117">-Force</span></span>
<span data-ttu-id="e7b51-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e7b51-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b51-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7b51-119">-Name</span></span>
<span data-ttu-id="e7b51-120">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e7b51-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="e7b51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b51-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7b51-122">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b51-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="e7b51-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7b51-123">-Confirm</span></span>
<span data-ttu-id="e7b51-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b51-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b51-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b51-125">-WhatIf</span></span>
<span data-ttu-id="e7b51-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b51-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b51-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7b51-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b51-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b51-128">CommonParameters</span></span>
<span data-ttu-id="e7b51-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b51-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b51-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b51-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b51-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7b51-131">INPUTS</span></span>

### <span data-ttu-id="e7b51-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7b51-132">System.String</span></span>

## <span data-ttu-id="e7b51-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7b51-133">OUTPUTS</span></span>

### <span data-ttu-id="e7b51-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e7b51-134">System.Void</span></span>

## <span data-ttu-id="e7b51-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7b51-135">NOTES</span></span>

## <span data-ttu-id="e7b51-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7b51-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7b51-137">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="e7b51-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="e7b51-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7b51-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


