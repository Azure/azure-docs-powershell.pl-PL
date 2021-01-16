---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335518"
---
# <span data-ttu-id="3fc17-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="3fc17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fc17-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc17-103">Pobiera istniejący profil sieciowy zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="3fc17-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="3fc17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fc17-104">SYNTAX</span></span>

### <span data-ttu-id="3fc17-105">GetByResourceNameNoExpandParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3fc17-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fc17-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fc17-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc17-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fc17-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fc17-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fc17-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc17-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3fc17-109">DESCRIPTION</span></span>
<span data-ttu-id="3fc17-110">Polecenie cmdlet **Get-AzNetworkProfile** pobiera istniejący profil sieci zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="3fc17-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="3fc17-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fc17-111">EXAMPLES</span></span>

### <span data-ttu-id="3fc17-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fc17-112">Example 1</span></span>
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

<span data-ttu-id="3fc17-113">Spowoduje to pobranie profilu NP1 w grupie zasób RG1</span><span class="sxs-lookup"><span data-stu-id="3fc17-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="3fc17-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3fc17-114">Example 2</span></span>
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

<span data-ttu-id="3fc17-115">Spowoduje to pobranie profilów sieciowych, które zaczynają się od "np"</span><span class="sxs-lookup"><span data-stu-id="3fc17-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="3fc17-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fc17-116">PARAMETERS</span></span>

### <span data-ttu-id="3fc17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-117">-DefaultProfile</span></span>
<span data-ttu-id="3fc17-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc17-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="3fc17-119">-ExpandResource</span></span>
<span data-ttu-id="3fc17-120">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="3fc17-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="3fc17-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fc17-121">-Name</span></span>
<span data-ttu-id="3fc17-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3fc17-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="3fc17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc17-123">-ResourceGroupName</span></span>
<span data-ttu-id="3fc17-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3fc17-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="3fc17-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fc17-125">-ResourceId</span></span>
<span data-ttu-id="3fc17-126">Identyfikator Menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3fc17-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="3fc17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc17-127">CommonParameters</span></span>
<span data-ttu-id="3fc17-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc17-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fc17-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc17-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fc17-130">INPUTS</span></span>

### <span data-ttu-id="3fc17-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3fc17-131">System.String</span></span>

## <span data-ttu-id="3fc17-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fc17-132">OUTPUTS</span></span>

### <span data-ttu-id="3fc17-133">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="3fc17-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fc17-134">NOTES</span></span>

## <span data-ttu-id="3fc17-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fc17-135">RELATED LINKS</span></span>

[<span data-ttu-id="3fc17-136">Nowe — AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="3fc17-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="3fc17-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fc17-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
