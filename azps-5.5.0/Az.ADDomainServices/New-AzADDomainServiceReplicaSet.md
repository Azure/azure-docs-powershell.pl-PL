---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176594"
---
# <span data-ttu-id="c0830-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c0830-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="c0830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0830-102">SYNOPSIS</span></span>
<span data-ttu-id="c0830-103">Tworzenie obiektu w pamięci dla zestawu ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c0830-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="c0830-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0830-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="c0830-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0830-105">DESCRIPTION</span></span>
<span data-ttu-id="c0830-106">Tworzenie obiektu w pamięci dla zestawu ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c0830-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="c0830-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0830-107">EXAMPLES</span></span>

### <span data-ttu-id="c0830-108">Przykład 1. Tworzenie zestawu replik dla domeny AdDomain</span><span class="sxs-lookup"><span data-stu-id="c0830-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="c0830-109">Tworzenie zestawu replik dla domeny AdDomain</span><span class="sxs-lookup"><span data-stu-id="c0830-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="c0830-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0830-110">PARAMETERS</span></span>

### <span data-ttu-id="c0830-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c0830-111">-Location</span></span>
<span data-ttu-id="c0830-112">Wirtualna lokalizacja sieciowa.</span><span class="sxs-lookup"><span data-stu-id="c0830-112">Virtual network location.</span></span>

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

### <span data-ttu-id="c0830-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c0830-113">-SubnetId</span></span>
<span data-ttu-id="c0830-114">Nazwa sieci wirtualnej, w przypadku których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="c0830-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="c0830-115">Identyfikator podsieci, w których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="c0830-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="c0830-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="c0830-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="c0830-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0830-117">CommonParameters</span></span>
<span data-ttu-id="c0830-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0830-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0830-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0830-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0830-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0830-120">INPUTS</span></span>

## <span data-ttu-id="c0830-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0830-121">OUTPUTS</span></span>

### <span data-ttu-id="c0830-122">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c0830-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="c0830-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0830-123">NOTES</span></span>

<span data-ttu-id="c0830-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c0830-124">ALIASES</span></span>

## <span data-ttu-id="c0830-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0830-125">RELATED LINKS</span></span>

