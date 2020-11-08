---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220012"
---
# <span data-ttu-id="28c4e-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="28c4e-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="28c4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="28c4e-103">Uzyskiwanie lub wyświetlanie witryn połączonych z zasobami sieciowymi na urządzeniu wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="28c4e-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="28c4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28c4e-104">SYNTAX</span></span>

### <span data-ttu-id="28c4e-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28c4e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28c4e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c4e-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28c4e-107">DESCRIPTION</span></span>
<span data-ttu-id="28c4e-108">Get-AzVirtualApplianceSite Pobiera lub wyświetla witryny połączone z jednym lub kilkoma zasobami sieciowymi urządzeń wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="28c4e-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="28c4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28c4e-109">EXAMPLES</span></span>

### <span data-ttu-id="28c4e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28c4e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="28c4e-111">Pobierz zasób witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="28c4e-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="28c4e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28c4e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="28c4e-113">Wyświetlanie zasobów witryny urządzenia wirtualnego w sieciowym urządzeniu wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="28c4e-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="28c4e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28c4e-114">PARAMETERS</span></span>

### <span data-ttu-id="28c4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c4e-115">-DefaultProfile</span></span>
<span data-ttu-id="28c4e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28c4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c4e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28c4e-117">-Name</span></span>
<span data-ttu-id="28c4e-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="28c4e-118">The resource name.</span></span>

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

### <span data-ttu-id="28c4e-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="28c4e-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="28c4e-120">Sieciowy wirtualny urządzenie, do którego dołączona jest witryna.</span><span class="sxs-lookup"><span data-stu-id="28c4e-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="28c4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="28c4e-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28c4e-122">The resource group name.</span></span>

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

### <span data-ttu-id="28c4e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28c4e-123">-ResourceId</span></span>
<span data-ttu-id="28c4e-124">Identyfikator zasobu witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="28c4e-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="28c4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c4e-125">CommonParameters</span></span>
<span data-ttu-id="28c4e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c4e-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c4e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c4e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28c4e-128">INPUTS</span></span>

### <span data-ttu-id="28c4e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="28c4e-129">System.String</span></span>

## <span data-ttu-id="28c4e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28c4e-130">OUTPUTS</span></span>

### <span data-ttu-id="28c4e-131">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="28c4e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="28c4e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28c4e-132">NOTES</span></span>

## <span data-ttu-id="28c4e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28c4e-133">RELATED LINKS</span></span>
