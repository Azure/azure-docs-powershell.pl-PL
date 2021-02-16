---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193810"
---
# <span data-ttu-id="01545-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="01545-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="01545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01545-102">SYNOPSIS</span></span>
<span data-ttu-id="01545-103">Pobierz lub na liście dostępne jednostki SKU wirtualnego urządzenia sieciowego w spisie.</span><span class="sxs-lookup"><span data-stu-id="01545-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="01545-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01545-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01545-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="01545-105">DESCRIPTION</span></span>
<span data-ttu-id="01545-106">Ten Get-AzNetworkVirtualApplianceSku pobiera lub wyświetla dostępne jednostki SKU wirtualnego urządzenia sieciowego w spisie produktów platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01545-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="01545-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01545-107">EXAMPLES</span></span>

### <span data-ttu-id="01545-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01545-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="01545-109">Pobierz sku według nazwy.</span><span class="sxs-lookup"><span data-stu-id="01545-109">Get a sku by name.</span></span>

### <span data-ttu-id="01545-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="01545-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="01545-111">Lista wszystkich dostępnych jednostki SKU urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="01545-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="01545-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01545-112">PARAMETERS</span></span>

### <span data-ttu-id="01545-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01545-113">-DefaultProfile</span></span>
<span data-ttu-id="01545-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01545-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01545-115">-SKUName</span><span class="sxs-lookup"><span data-stu-id="01545-115">-SkuName</span></span>
<span data-ttu-id="01545-116">Nazwa sku.</span><span class="sxs-lookup"><span data-stu-id="01545-116">The Sku name.</span></span>

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

### <span data-ttu-id="01545-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01545-117">CommonParameters</span></span>
<span data-ttu-id="01545-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01545-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01545-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01545-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01545-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01545-120">INPUTS</span></span>

### <span data-ttu-id="01545-121">Brak</span><span class="sxs-lookup"><span data-stu-id="01545-121">None</span></span>

## <span data-ttu-id="01545-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01545-122">OUTPUTS</span></span>

### <span data-ttu-id="01545-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="01545-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="01545-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01545-124">NOTES</span></span>

## <span data-ttu-id="01545-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01545-125">RELATED LINKS</span></span>
