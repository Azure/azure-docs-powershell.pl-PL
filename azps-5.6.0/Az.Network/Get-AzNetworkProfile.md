---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: f2f18ac77f923247f2bef0e78802a2f05cf302d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954538"
---
# <span data-ttu-id="b7e14-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="b7e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e14-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e14-103">Pobiera istniejący zasób najwyższego poziomu profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="b7e14-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="b7e14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7e14-104">SYNTAX</span></span>

### <span data-ttu-id="b7e14-105">GetByResourceNameNoExpandParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b7e14-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e14-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e14-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7e14-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e14-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e14-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e14-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7e14-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7e14-109">DESCRIPTION</span></span>
<span data-ttu-id="b7e14-110">Polecenie **cmdlet Get-AzNetworkProfile** pobiera istniejący zasób najwyższego poziomu profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="b7e14-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="b7e14-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7e14-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e14-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7e14-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="b7e14-113">To pobiera profil sieciowy np1 w grupie zasobów nr rg1</span><span class="sxs-lookup"><span data-stu-id="b7e14-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="b7e14-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b7e14-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="b7e14-115">W ten sposób są pobierane profile sieciowe, które zaczynają się od "np".</span><span class="sxs-lookup"><span data-stu-id="b7e14-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="b7e14-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7e14-116">PARAMETERS</span></span>

### <span data-ttu-id="b7e14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-117">-DefaultProfile</span></span>
<span data-ttu-id="b7e14-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e14-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e14-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b7e14-119">-ExpandResource</span></span>
<span data-ttu-id="b7e14-120">Odwołanie do zasobu do rozwinięcia.</span><span class="sxs-lookup"><span data-stu-id="b7e14-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e14-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7e14-121">-Name</span></span>
<span data-ttu-id="b7e14-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b7e14-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7e14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e14-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7e14-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b7e14-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7e14-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e14-125">-ResourceId</span></span>
<span data-ttu-id="b7e14-126">Identyfikator menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b7e14-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e14-127">CommonParameters</span></span>
<span data-ttu-id="b7e14-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e14-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7e14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e14-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e14-130">INPUTS</span></span>

### <span data-ttu-id="b7e14-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e14-131">System.String</span></span>

## <span data-ttu-id="b7e14-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e14-132">OUTPUTS</span></span>

### <span data-ttu-id="b7e14-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b7e14-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7e14-134">NOTES</span></span>

## <span data-ttu-id="b7e14-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7e14-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7e14-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="b7e14-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="b7e14-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e14-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
