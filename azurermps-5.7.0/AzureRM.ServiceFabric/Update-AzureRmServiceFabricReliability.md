---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 5b88342a91f015cd58da36f9b04d3a8a325ae239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526566"
---
# <span data-ttu-id="c6801-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="c6801-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="c6801-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6801-102">SYNOPSIS</span></span>
<span data-ttu-id="c6801-103">Aktualizowanie warstwy niezawodności typu węzła podstawowego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="c6801-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6801-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6801-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6801-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6801-105">DESCRIPTION</span></span>
<span data-ttu-id="c6801-106">W celu zaktualizowania niezawodności podstawowego typu węzła w klastrze Użyj funkcji **Update-AzureRmServiceFabricReliability** .</span><span class="sxs-lookup"><span data-stu-id="c6801-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="c6801-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6801-107">EXAMPLES</span></span>

### <span data-ttu-id="c6801-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6801-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="c6801-109">To polecenie powoduje zmianę warstwy niezawodności typu węzła podstawowego na srebrny.</span><span class="sxs-lookup"><span data-stu-id="c6801-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="c6801-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6801-110">PARAMETERS</span></span>

### <span data-ttu-id="c6801-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="c6801-111">-AutoAddNode</span></span>
<span data-ttu-id="c6801-112">Automatyczne dodawanie liczby węzłów podczas zmieniania niezawodności.</span><span class="sxs-lookup"><span data-stu-id="c6801-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6801-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6801-113">-DefaultProfile</span></span>
<span data-ttu-id="c6801-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6801-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6801-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6801-115">-Name</span></span>
<span data-ttu-id="c6801-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="c6801-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6801-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c6801-117">-ReliabilityLevel</span></span>
<span data-ttu-id="c6801-118">Warstwa niezawodności.</span><span class="sxs-lookup"><span data-stu-id="c6801-118">Reliability tier.</span></span>

```yaml
Type: ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6801-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6801-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6801-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6801-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6801-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6801-121">-Confirm</span></span>
<span data-ttu-id="c6801-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6801-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6801-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6801-123">-WhatIf</span></span>
<span data-ttu-id="c6801-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6801-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6801-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6801-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6801-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6801-126">CommonParameters</span></span>
<span data-ttu-id="c6801-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6801-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6801-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6801-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6801-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6801-129">INPUTS</span></span>

### <span data-ttu-id="c6801-130">Microsoft. Azure. Commands. servicefabric. MODELES. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c6801-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="c6801-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c6801-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="c6801-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c6801-132">System.String</span></span>

## <span data-ttu-id="c6801-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6801-133">OUTPUTS</span></span>

### <span data-ttu-id="c6801-134">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="c6801-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="c6801-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6801-135">NOTES</span></span>

## <span data-ttu-id="c6801-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6801-136">RELATED LINKS</span></span>

