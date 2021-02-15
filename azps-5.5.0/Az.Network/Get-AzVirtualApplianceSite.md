---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193723"
---
# <span data-ttu-id="a1069-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a1069-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a1069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1069-102">SYNOPSIS</span></span>
<span data-ttu-id="a1069-103">Uzyskiwanie lub listy witryn połączonych z zasobami funkcji Network Virtual Przygotowawczy.</span><span class="sxs-lookup"><span data-stu-id="a1069-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="a1069-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1069-104">SYNTAX</span></span>

### <span data-ttu-id="a1069-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a1069-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1069-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1069-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1069-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1069-107">DESCRIPTION</span></span>
<span data-ttu-id="a1069-108">Ta Get-AzVirtualApplianceSite pobiera lub wyświetla witryny połączone z co najmniej jednym zasobem wirtualnego urządzenia network.</span><span class="sxs-lookup"><span data-stu-id="a1069-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="a1069-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1069-109">EXAMPLES</span></span>

### <span data-ttu-id="a1069-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1069-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="a1069-111">Uzyskaj zasób witryny Urządzenie wirtualne.</span><span class="sxs-lookup"><span data-stu-id="a1069-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="a1069-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a1069-112">Example 2</span></span>
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

<span data-ttu-id="a1069-113">Lista zasobów witryny Wirtualne urządzenie w urządzeniu wirtualnym sieci.</span><span class="sxs-lookup"><span data-stu-id="a1069-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="a1069-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1069-114">PARAMETERS</span></span>

### <span data-ttu-id="a1069-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1069-115">-DefaultProfile</span></span>
<span data-ttu-id="a1069-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1069-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1069-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1069-117">-Name</span></span>
<span data-ttu-id="a1069-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1069-118">The resource name.</span></span>

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

### <span data-ttu-id="a1069-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a1069-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a1069-120">Urządzenie wirtualne sieci, do których dołączono witrynę.</span><span class="sxs-lookup"><span data-stu-id="a1069-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="a1069-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1069-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1069-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1069-122">The resource group name.</span></span>

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

### <span data-ttu-id="a1069-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1069-123">-ResourceId</span></span>
<span data-ttu-id="a1069-124">Identyfikator zasobu w witrynie wirtualnego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a1069-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="a1069-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1069-125">CommonParameters</span></span>
<span data-ttu-id="a1069-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1069-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1069-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1069-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1069-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1069-128">INPUTS</span></span>

### <span data-ttu-id="a1069-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a1069-129">System.String</span></span>

## <span data-ttu-id="a1069-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1069-130">OUTPUTS</span></span>

### <span data-ttu-id="a1069-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a1069-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a1069-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1069-132">NOTES</span></span>

## <span data-ttu-id="a1069-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1069-133">RELATED LINKS</span></span>
