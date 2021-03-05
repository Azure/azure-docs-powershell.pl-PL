---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 916e818b628608fcae7001797af298317ff96a4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989759"
---
# <span data-ttu-id="a9c2a-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9c2a-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a9c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c2a-103">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-103">Removes a workspace.</span></span>

## <span data-ttu-id="a9c2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9c2a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c2a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c2a-106">Polecenie **cmdlet Remove-AzOperationalInsightsWorkspace** usuwa istniejący obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="a9c2a-107">Jeśli w momencie utworzenia tego obszaru roboczego ten obszar roboczy został połączony z istniejącym kontem za pośrednictwem parametru *CustomerId,* oryginalne konto nie zostanie usunięte w portalu Informacje operacyjne.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="a9c2a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9c2a-108">EXAMPLES</span></span>

### <span data-ttu-id="a9c2a-109">Przykład 1. Usuwanie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="a9c2a-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a9c2a-110">To polecenie usuwa obszar roboczy o nazwie MyWorkspace z grupy zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a9c2a-111">Przykład 2. Usuwanie obszaru roboczego przy użyciu potoku i bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="a9c2a-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="a9c2a-112">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie przekazuje je do polecenia cmdlet **Remove-AzOperationalInsightsWorkspace** przy użyciu operatora potoku w celu jego usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="a9c2a-113">Ponieważ parametr *Force* jest określony, polecenie nie wyświetla monitu przed usunięciem obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="a9c2a-114">Przykład 3. Wymuszanie usunięcia obszaru roboczego (nie można go odzyskać)</span><span class="sxs-lookup"><span data-stu-id="a9c2a-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="a9c2a-115">Wymuszanie usunięcia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-115">Force delete a workspace.</span></span>

## <span data-ttu-id="a9c2a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9c2a-116">PARAMETERS</span></span>

### <span data-ttu-id="a9c2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c2a-117">-DefaultProfile</span></span>
<span data-ttu-id="a9c2a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a9c2a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9c2a-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a9c2a-119">-Force</span></span>
<span data-ttu-id="a9c2a-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9c2a-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="a9c2a-121">-ForceDelete</span></span>
<span data-ttu-id="a9c2a-122">Wymuszanie usunięcia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="a9c2a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9c2a-123">-Name</span></span>
<span data-ttu-id="a9c2a-124">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="a9c2a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c2a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9c2a-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="a9c2a-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9c2a-127">-Confirm</span></span>
<span data-ttu-id="a9c2a-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c2a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c2a-129">-WhatIf</span></span>
<span data-ttu-id="a9c2a-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c2a-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c2a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c2a-132">CommonParameters</span></span>
<span data-ttu-id="a9c2a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c2a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c2a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c2a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c2a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9c2a-135">INPUTS</span></span>

### <span data-ttu-id="a9c2a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a9c2a-136">System.String</span></span>

## <span data-ttu-id="a9c2a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9c2a-137">OUTPUTS</span></span>

### <span data-ttu-id="a9c2a-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="a9c2a-138">System.Void</span></span>

## <span data-ttu-id="a9c2a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9c2a-139">NOTES</span></span>

## <span data-ttu-id="a9c2a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9c2a-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9c2a-141">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="a9c2a-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a9c2a-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9c2a-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


