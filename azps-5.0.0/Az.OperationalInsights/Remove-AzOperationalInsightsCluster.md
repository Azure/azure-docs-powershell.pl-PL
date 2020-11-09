---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308046"
---
# <span data-ttu-id="5cc8c-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="5cc8c-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="5cc8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc8c-103">Usuń klaster</span><span class="sxs-lookup"><span data-stu-id="5cc8c-103">Delete cluster</span></span>

## <span data-ttu-id="5cc8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cc8c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5cc8c-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc8c-106">Usuń klaster, Zastosuj tylko do klastrów z stanem inicjowania obsługi "powiodło się"</span><span class="sxs-lookup"><span data-stu-id="5cc8c-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="5cc8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cc8c-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc8c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5cc8c-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="5cc8c-109">Usuń klaster</span><span class="sxs-lookup"><span data-stu-id="5cc8c-109">Delete cluster</span></span>

## <span data-ttu-id="5cc8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cc8c-110">PARAMETERS</span></span>

### <span data-ttu-id="5cc8c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cc8c-111">-AsJob</span></span>
<span data-ttu-id="5cc8c-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5cc8c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cc8c-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="5cc8c-113">-ClusterName</span></span>
<span data-ttu-id="5cc8c-114">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-114">The cluster name.</span></span>

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

### <span data-ttu-id="5cc8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc8c-115">-DefaultProfile</span></span>
<span data-ttu-id="5cc8c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cc8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cc8c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-118">The resource group name.</span></span>

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

### <span data-ttu-id="5cc8c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cc8c-119">-Confirm</span></span>
<span data-ttu-id="5cc8c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc8c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc8c-121">-WhatIf</span></span>
<span data-ttu-id="5cc8c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc8c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc8c-124">CommonParameters</span></span>
<span data-ttu-id="5cc8c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc8c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cc8c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc8c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cc8c-127">INPUTS</span></span>

### <span data-ttu-id="5cc8c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc8c-128">System.String</span></span>

## <span data-ttu-id="5cc8c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cc8c-129">OUTPUTS</span></span>

### <span data-ttu-id="5cc8c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5cc8c-130">System.Boolean</span></span>

## <span data-ttu-id="5cc8c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cc8c-131">NOTES</span></span>

## <span data-ttu-id="5cc8c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cc8c-132">RELATED LINKS</span></span>
