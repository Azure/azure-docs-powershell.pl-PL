---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: b0630a1d7fee588716c4db493f9c5ead2003165c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708065"
---
# <span data-ttu-id="9fda6-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="9fda6-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="9fda6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fda6-102">SYNOPSIS</span></span>
<span data-ttu-id="9fda6-103">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="9fda6-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="9fda6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fda6-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fda6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fda6-105">DESCRIPTION</span></span>
<span data-ttu-id="9fda6-106">W celu zaktualizowania niezawodności podstawowego typu węzła w klastrze Użyj funkcji **Update-AzServiceFabricReliability** .</span><span class="sxs-lookup"><span data-stu-id="9fda6-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="9fda6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fda6-107">EXAMPLES</span></span>

### <span data-ttu-id="9fda6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9fda6-108">Example 1</span></span>
```
PS c:> Add-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="9fda6-109">To polecenie powoduje zmianę warstwy niezawodności typu węzła podstawowego na srebrny.</span><span class="sxs-lookup"><span data-stu-id="9fda6-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="9fda6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fda6-110">PARAMETERS</span></span>

### <span data-ttu-id="9fda6-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="9fda6-111">-AutoAddNode</span></span>
<span data-ttu-id="9fda6-112">Automatyczne dodawanie liczby węzłów podczas zmieniania niezawodności.</span><span class="sxs-lookup"><span data-stu-id="9fda6-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="9fda6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fda6-113">-DefaultProfile</span></span>
<span data-ttu-id="9fda6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fda6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fda6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fda6-115">-Name</span></span>
<span data-ttu-id="9fda6-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9fda6-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9fda6-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9fda6-117">-ReliabilityLevel</span></span>
<span data-ttu-id="9fda6-118">Warstwa niezawodności.</span><span class="sxs-lookup"><span data-stu-id="9fda6-118">Reliability tier.</span></span>

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

### <span data-ttu-id="9fda6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fda6-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fda6-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fda6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9fda6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fda6-121">-Confirm</span></span>
<span data-ttu-id="9fda6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fda6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fda6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fda6-123">-WhatIf</span></span>
<span data-ttu-id="9fda6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fda6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fda6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fda6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fda6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fda6-126">CommonParameters</span></span>
<span data-ttu-id="9fda6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fda6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fda6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fda6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fda6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fda6-129">INPUTS</span></span>

### <span data-ttu-id="9fda6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9fda6-130">System.String</span></span>

### <span data-ttu-id="9fda6-131">Microsoft. Azure. Commands. servicefabric. MODELES. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9fda6-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="9fda6-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fda6-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fda6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fda6-133">OUTPUTS</span></span>

### <span data-ttu-id="9fda6-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9fda6-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9fda6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fda6-135">NOTES</span></span>

## <span data-ttu-id="9fda6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fda6-136">RELATED LINKS</span></span>
