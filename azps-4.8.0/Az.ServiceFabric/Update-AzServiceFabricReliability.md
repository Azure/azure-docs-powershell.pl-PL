---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222262"
---
# <span data-ttu-id="a17d3-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a17d3-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="a17d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a17d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a17d3-103">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="a17d3-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="a17d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a17d3-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a17d3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a17d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a17d3-106">W celu zaktualizowania niezawodności podstawowego typu węzła w klastrze Użyj funkcji **Update-AzServiceFabricReliability** .</span><span class="sxs-lookup"><span data-stu-id="a17d3-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="a17d3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a17d3-107">EXAMPLES</span></span>

### <span data-ttu-id="a17d3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a17d3-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="a17d3-109">To polecenie powoduje zmianę warstwy niezawodności typu węzła podstawowego na srebrny.</span><span class="sxs-lookup"><span data-stu-id="a17d3-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="a17d3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a17d3-110">PARAMETERS</span></span>

### <span data-ttu-id="a17d3-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="a17d3-111">-AutoAddNode</span></span>
<span data-ttu-id="a17d3-112">Automatyczne dodawanie liczby węzłów podczas zmieniania niezawodności</span><span class="sxs-lookup"><span data-stu-id="a17d3-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a17d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17d3-113">-DefaultProfile</span></span>
<span data-ttu-id="a17d3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a17d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a17d3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a17d3-115">-Name</span></span>
<span data-ttu-id="a17d3-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="a17d3-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17d3-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a17d3-117">-ReliabilityLevel</span></span>
<span data-ttu-id="a17d3-118">Warstwa niezawodności</span><span class="sxs-lookup"><span data-stu-id="a17d3-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a17d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a17d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a17d3-120">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a17d3-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a17d3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a17d3-121">-Confirm</span></span>
<span data-ttu-id="a17d3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a17d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a17d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a17d3-123">-WhatIf</span></span>
<span data-ttu-id="a17d3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a17d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a17d3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a17d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a17d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17d3-126">CommonParameters</span></span>
<span data-ttu-id="a17d3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a17d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17d3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a17d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17d3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a17d3-129">INPUTS</span></span>

### <span data-ttu-id="a17d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a17d3-130">System.String</span></span>

### <span data-ttu-id="a17d3-131">Microsoft. Azure. Commands. servicefabric. MODELES. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a17d3-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="a17d3-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a17d3-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a17d3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a17d3-133">OUTPUTS</span></span>

### <span data-ttu-id="a17d3-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a17d3-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a17d3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a17d3-135">NOTES</span></span>

## <span data-ttu-id="a17d3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a17d3-136">RELATED LINKS</span></span>
