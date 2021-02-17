---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202335"
---
# <span data-ttu-id="c0483-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="c0483-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="c0483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0483-102">SYNOPSIS</span></span>
<span data-ttu-id="c0483-103">Usuwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="c0483-103">Delete cluster</span></span>

## <span data-ttu-id="c0483-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0483-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0483-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0483-105">DESCRIPTION</span></span>
<span data-ttu-id="c0483-106">Usuwanie klastrów, stosowanie tylko do klastrów ze stanem inicjowania obsługi "Pomyślnie"</span><span class="sxs-lookup"><span data-stu-id="c0483-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="c0483-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0483-107">EXAMPLES</span></span>

### <span data-ttu-id="c0483-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0483-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="c0483-109">Usuwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="c0483-109">Delete cluster</span></span>

## <span data-ttu-id="c0483-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0483-110">PARAMETERS</span></span>

### <span data-ttu-id="c0483-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c0483-111">-AsJob</span></span>
<span data-ttu-id="c0483-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c0483-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0483-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0483-113">-ClusterName</span></span>
<span data-ttu-id="c0483-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="c0483-114">The cluster name.</span></span>

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

### <span data-ttu-id="c0483-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0483-115">-DefaultProfile</span></span>
<span data-ttu-id="c0483-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0483-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0483-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0483-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0483-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0483-118">The resource group name.</span></span>

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

### <span data-ttu-id="c0483-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0483-119">-Confirm</span></span>
<span data-ttu-id="c0483-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0483-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0483-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0483-121">-WhatIf</span></span>
<span data-ttu-id="c0483-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0483-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0483-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0483-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0483-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0483-124">CommonParameters</span></span>
<span data-ttu-id="c0483-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0483-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0483-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0483-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0483-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0483-127">INPUTS</span></span>

### <span data-ttu-id="c0483-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c0483-128">System.String</span></span>

## <span data-ttu-id="c0483-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0483-129">OUTPUTS</span></span>

### <span data-ttu-id="c0483-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0483-130">System.Boolean</span></span>

## <span data-ttu-id="c0483-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0483-131">NOTES</span></span>

## <span data-ttu-id="c0483-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0483-132">RELATED LINKS</span></span>
