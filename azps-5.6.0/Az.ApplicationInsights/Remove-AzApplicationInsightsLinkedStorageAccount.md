---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001889"
---
# <span data-ttu-id="65381-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65381-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="65381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65381-102">SYNOPSIS</span></span>
<span data-ttu-id="65381-103">Usuwanie połączonego konta magazynu aplikacji Insights</span><span class="sxs-lookup"><span data-stu-id="65381-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="65381-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65381-104">SYNTAX</span></span>

### <span data-ttu-id="65381-105">ByResourceNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="65381-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65381-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65381-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65381-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65381-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65381-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="65381-108">DESCRIPTION</span></span>
<span data-ttu-id="65381-109">Usuwanie połączonego konta magazynu aplikacji Insights</span><span class="sxs-lookup"><span data-stu-id="65381-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="65381-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65381-110">EXAMPLES</span></span>

### <span data-ttu-id="65381-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65381-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="65381-112">Usuwanie połączonego konta magazynu skojarzonego ze składnikiem Szczegółowe informacje o aplikacji "componentName"</span><span class="sxs-lookup"><span data-stu-id="65381-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="65381-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65381-113">PARAMETERS</span></span>

### <span data-ttu-id="65381-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="65381-114">-ComponentName</span></span>
<span data-ttu-id="65381-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="65381-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65381-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65381-116">-DefaultProfile</span></span>
<span data-ttu-id="65381-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65381-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65381-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65381-118">-InputObject</span></span>
<span data-ttu-id="65381-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65381-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65381-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65381-120">-ResourceGroupName</span></span>
<span data-ttu-id="65381-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65381-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65381-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65381-122">-ResourceId</span></span>
<span data-ttu-id="65381-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="65381-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65381-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65381-124">-Confirm</span></span>
<span data-ttu-id="65381-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65381-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65381-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65381-126">-WhatIf</span></span>
<span data-ttu-id="65381-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65381-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65381-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65381-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65381-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65381-129">CommonParameters</span></span>
<span data-ttu-id="65381-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65381-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65381-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65381-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65381-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65381-132">INPUTS</span></span>

### <span data-ttu-id="65381-133">System.String</span><span class="sxs-lookup"><span data-stu-id="65381-133">System.String</span></span>

### <span data-ttu-id="65381-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65381-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="65381-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65381-135">OUTPUTS</span></span>

### <span data-ttu-id="65381-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65381-136">System.Boolean</span></span>

## <span data-ttu-id="65381-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65381-137">NOTES</span></span>

## <span data-ttu-id="65381-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65381-138">RELATED LINKS</span></span>
