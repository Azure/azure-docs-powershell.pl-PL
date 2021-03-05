---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: ad11cbe364cd4d9cd8a667fd40a6a1d438f1aed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986308"
---
# <span data-ttu-id="e8498-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="e8498-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="e8498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8498-102">SYNOPSIS</span></span>
<span data-ttu-id="e8498-103">Tworzenie obiektu w pamięci dla zestawu ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="e8498-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="e8498-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8498-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e8498-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8498-105">DESCRIPTION</span></span>
<span data-ttu-id="e8498-106">Tworzenie obiektu w pamięci dla zestawu ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="e8498-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="e8498-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8498-107">EXAMPLES</span></span>

### <span data-ttu-id="e8498-108">Przykład 1. Tworzenie zestawu replik dla domeny AdDomain</span><span class="sxs-lookup"><span data-stu-id="e8498-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="e8498-109">Tworzenie zestawu replik dla domeny AdDomain</span><span class="sxs-lookup"><span data-stu-id="e8498-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="e8498-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8498-110">PARAMETERS</span></span>

### <span data-ttu-id="e8498-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8498-111">-Location</span></span>
<span data-ttu-id="e8498-112">Wirtualna lokalizacja sieciowa.</span><span class="sxs-lookup"><span data-stu-id="e8498-112">Virtual network location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8498-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8498-113">-SubnetId</span></span>
<span data-ttu-id="e8498-114">Nazwa sieci wirtualnej, w przypadku których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="e8498-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="e8498-115">Identyfikator podsieci, w których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="e8498-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="e8498-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="e8498-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8498-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8498-117">CommonParameters</span></span>
<span data-ttu-id="e8498-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8498-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8498-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8498-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8498-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8498-120">INPUTS</span></span>

## <span data-ttu-id="e8498-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8498-121">OUTPUTS</span></span>

### <span data-ttu-id="e8498-122">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="e8498-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="e8498-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8498-123">NOTES</span></span>

<span data-ttu-id="e8498-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e8498-124">ALIASES</span></span>

## <span data-ttu-id="e8498-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8498-125">RELATED LINKS</span></span>

