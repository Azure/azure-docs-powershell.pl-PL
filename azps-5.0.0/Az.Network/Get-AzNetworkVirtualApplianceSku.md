---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224946"
---
# <span data-ttu-id="b3bc2-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b3bc2-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b3bc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bc2-103">Uzyskaj lub Wyświetl listę dostępnych w magazynie jednostek SKU urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="b3bc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3bc2-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3bc2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bc2-106">Get-AzNetworkVirtualApplianceSku Pobiera lub wyświetla dostępne jednostki SKU sieciowych urządzeń wirtualnych w magazynie Microsoft Azure Inventory.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="b3bc2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="b3bc2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3bc2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="b3bc2-109">Pobierz jednostkę SKU według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-109">Get a sku by name.</span></span>

### <span data-ttu-id="b3bc2-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b3bc2-110">Example 2</span></span>
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

<span data-ttu-id="b3bc2-111">Wyświetl wszystkie dostępne jednostki SKU wirtualnego urządzenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="b3bc2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3bc2-112">PARAMETERS</span></span>

### <span data-ttu-id="b3bc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bc2-113">-DefaultProfile</span></span>
<span data-ttu-id="b3bc2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3bc2-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b3bc2-115">-SkuName</span></span>
<span data-ttu-id="b3bc2-116">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-116">The Sku name.</span></span>

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

### <span data-ttu-id="b3bc2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bc2-117">CommonParameters</span></span>
<span data-ttu-id="b3bc2-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bc2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bc2-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3bc2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bc2-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3bc2-120">INPUTS</span></span>

### <span data-ttu-id="b3bc2-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3bc2-121">None</span></span>

## <span data-ttu-id="b3bc2-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3bc2-122">OUTPUTS</span></span>

### <span data-ttu-id="b3bc2-123">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b3bc2-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b3bc2-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3bc2-124">NOTES</span></span>

## <span data-ttu-id="b3bc2-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3bc2-125">RELATED LINKS</span></span>
