---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: b2cb61ff6b80cb6e0325f006d063d7e0a8971a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989871"
---
# <span data-ttu-id="0dfc8-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="0dfc8-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="0dfc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dfc8-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfc8-103">Usuwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="0dfc8-103">Delete cluster</span></span>

## <span data-ttu-id="0dfc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0dfc8-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dfc8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0dfc8-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfc8-106">Usuwanie klastrów, stosowanie tylko do klastrów ze stanem inicjowania obsługi "Pomyślnie"</span><span class="sxs-lookup"><span data-stu-id="0dfc8-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="0dfc8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0dfc8-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfc8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0dfc8-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="0dfc8-109">Usuwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="0dfc8-109">Delete cluster</span></span>

## <span data-ttu-id="0dfc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dfc8-110">PARAMETERS</span></span>

### <span data-ttu-id="0dfc8-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0dfc8-111">-AsJob</span></span>
<span data-ttu-id="0dfc8-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0dfc8-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0dfc8-113">-ClusterName</span></span>
<span data-ttu-id="0dfc8-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfc8-115">-DefaultProfile</span></span>
<span data-ttu-id="0dfc8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dfc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="0dfc8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0dfc8-119">-Confirm</span></span>
<span data-ttu-id="0dfc8-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfc8-121">-WhatIf</span></span>
<span data-ttu-id="0dfc8-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dfc8-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfc8-124">CommonParameters</span></span>
<span data-ttu-id="0dfc8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dfc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfc8-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dfc8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfc8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dfc8-127">INPUTS</span></span>

### <span data-ttu-id="0dfc8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0dfc8-128">System.String</span></span>

## <span data-ttu-id="0dfc8-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dfc8-129">OUTPUTS</span></span>

### <span data-ttu-id="0dfc8-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0dfc8-130">System.Boolean</span></span>

## <span data-ttu-id="0dfc8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0dfc8-131">NOTES</span></span>

## <span data-ttu-id="0dfc8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dfc8-132">RELATED LINKS</span></span>
