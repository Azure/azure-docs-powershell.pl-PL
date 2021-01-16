---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379995"
---
# <span data-ttu-id="c2afb-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="c2afb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2afb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2afb-103">Pobiera istniejący profil sieciowy zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="c2afb-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="c2afb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2afb-104">SYNTAX</span></span>

### <span data-ttu-id="c2afb-105">GetByResourceNameNoExpandParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2afb-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2afb-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2afb-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2afb-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2afb-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2afb-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2afb-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2afb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c2afb-109">DESCRIPTION</span></span>
<span data-ttu-id="c2afb-110">Polecenie cmdlet **Get-AzNetworkProfile** pobiera istniejący profil sieci zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="c2afb-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="c2afb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2afb-111">EXAMPLES</span></span>

### <span data-ttu-id="c2afb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2afb-112">Example 1</span></span>
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

<span data-ttu-id="c2afb-113">Spowoduje to pobranie profilu NP1 w grupie zasób RG1</span><span class="sxs-lookup"><span data-stu-id="c2afb-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="c2afb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2afb-114">Example 2</span></span>
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

<span data-ttu-id="c2afb-115">Spowoduje to pobranie profilów sieciowych, które zaczynają się od "np"</span><span class="sxs-lookup"><span data-stu-id="c2afb-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="c2afb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2afb-116">PARAMETERS</span></span>

### <span data-ttu-id="c2afb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-117">-DefaultProfile</span></span>
<span data-ttu-id="c2afb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2afb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2afb-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c2afb-119">-ExpandResource</span></span>
<span data-ttu-id="c2afb-120">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="c2afb-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="c2afb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2afb-121">-Name</span></span>
<span data-ttu-id="c2afb-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c2afb-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="c2afb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2afb-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2afb-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c2afb-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="c2afb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2afb-125">-ResourceId</span></span>
<span data-ttu-id="c2afb-126">Identyfikator Menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c2afb-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="c2afb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2afb-127">CommonParameters</span></span>
<span data-ttu-id="c2afb-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2afb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2afb-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2afb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2afb-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2afb-130">INPUTS</span></span>

### <span data-ttu-id="c2afb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c2afb-131">System.String</span></span>

## <span data-ttu-id="c2afb-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2afb-132">OUTPUTS</span></span>

### <span data-ttu-id="c2afb-133">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c2afb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2afb-134">NOTES</span></span>

## <span data-ttu-id="c2afb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2afb-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2afb-136">Nowe — AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="c2afb-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="c2afb-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2afb-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
