---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224950"
---
# <span data-ttu-id="6d05c-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6d05c-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6d05c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d05c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d05c-103">Uzyskaj lub Wyświetl listę urządzeń wirtualnych w sieci.</span><span class="sxs-lookup"><span data-stu-id="6d05c-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="6d05c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d05c-104">SYNTAX</span></span>

### <span data-ttu-id="6d05c-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d05c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d05c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d05c-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d05c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d05c-107">DESCRIPTION</span></span>
<span data-ttu-id="6d05c-108">Polecenia Get-AzNetworkVirtualAppliance pobierają lub wyświetlają zasoby sieciowych urządzeń wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="6d05c-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="6d05c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d05c-109">EXAMPLES</span></span>

### <span data-ttu-id="6d05c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d05c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="6d05c-111">Pobierz zasób sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6d05c-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6d05c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d05c-112">PARAMETERS</span></span>

### <span data-ttu-id="6d05c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d05c-113">-DefaultProfile</span></span>
<span data-ttu-id="6d05c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d05c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d05c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d05c-115">-Name</span></span>
<span data-ttu-id="6d05c-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d05c-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d05c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d05c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d05c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d05c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d05c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d05c-119">-ResourceId</span></span>
<span data-ttu-id="6d05c-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d05c-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d05c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d05c-121">CommonParameters</span></span>
<span data-ttu-id="6d05c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d05c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d05c-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d05c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d05c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d05c-124">INPUTS</span></span>

### <span data-ttu-id="6d05c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6d05c-125">System.String</span></span>

## <span data-ttu-id="6d05c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d05c-126">OUTPUTS</span></span>

### <span data-ttu-id="6d05c-127">Microsoft. Azure. Commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6d05c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6d05c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d05c-128">NOTES</span></span>

## <span data-ttu-id="6d05c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d05c-129">RELATED LINKS</span></span>
