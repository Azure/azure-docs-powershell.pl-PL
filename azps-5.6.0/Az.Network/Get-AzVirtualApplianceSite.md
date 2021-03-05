---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016209"
---
# <span data-ttu-id="c01a7-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="c01a7-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="c01a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c01a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c01a7-103">Uzyskiwanie lub listy witryn połączonych z zasobami funkcji Network Virtual Przygotowawczy.</span><span class="sxs-lookup"><span data-stu-id="c01a7-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="c01a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c01a7-104">SYNTAX</span></span>

### <span data-ttu-id="c01a7-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c01a7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c01a7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c01a7-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c01a7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c01a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c01a7-108">Witryna Get-AzVirtualApplianceSite pobiera lub wyświetla witryny połączone z co najmniej jednym zasobem urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="c01a7-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="c01a7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c01a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c01a7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c01a7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="c01a7-111">Uzyskaj zasób witryny Wirtualne urządzenie.</span><span class="sxs-lookup"><span data-stu-id="c01a7-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="c01a7-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c01a7-112">Example 2</span></span>
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

<span data-ttu-id="c01a7-113">Lista zasobów witryny wirtualnego urządzenia w urządzeniu wirtualnym sieci.</span><span class="sxs-lookup"><span data-stu-id="c01a7-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="c01a7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c01a7-114">PARAMETERS</span></span>

### <span data-ttu-id="c01a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c01a7-115">-DefaultProfile</span></span>
<span data-ttu-id="c01a7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c01a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c01a7-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c01a7-117">-Name</span></span>
<span data-ttu-id="c01a7-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c01a7-118">The resource name.</span></span>

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

### <span data-ttu-id="c01a7-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="c01a7-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="c01a7-120">Urządzenie wirtualne sieci, do których dołączono witrynę.</span><span class="sxs-lookup"><span data-stu-id="c01a7-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="c01a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c01a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="c01a7-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c01a7-122">The resource group name.</span></span>

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

### <span data-ttu-id="c01a7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c01a7-123">-ResourceId</span></span>
<span data-ttu-id="c01a7-124">Identyfikator zasobu w witrynie wirtualnego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="c01a7-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="c01a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01a7-125">CommonParameters</span></span>
<span data-ttu-id="c01a7-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c01a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01a7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c01a7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01a7-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c01a7-128">INPUTS</span></span>

### <span data-ttu-id="c01a7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c01a7-129">System.String</span></span>

## <span data-ttu-id="c01a7-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c01a7-130">OUTPUTS</span></span>

### <span data-ttu-id="c01a7-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="c01a7-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="c01a7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c01a7-132">NOTES</span></span>

## <span data-ttu-id="c01a7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c01a7-133">RELATED LINKS</span></span>
