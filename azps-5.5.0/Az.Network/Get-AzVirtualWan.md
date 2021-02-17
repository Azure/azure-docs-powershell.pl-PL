---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184579"
---
# <span data-ttu-id="10796-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="10796-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="10796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10796-102">SYNOPSIS</span></span>
<span data-ttu-id="10796-103">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10796-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="10796-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10796-104">SYNTAX</span></span>

### <span data-ttu-id="10796-105">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10796-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10796-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10796-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10796-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="10796-107">DESCRIPTION</span></span>
<span data-ttu-id="10796-108">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10796-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="10796-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10796-109">EXAMPLES</span></span>

### <span data-ttu-id="10796-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10796-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="10796-111">To polecenie pobiera wirtualną sieć WAN o nazwie myVirtualWAN w testRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10796-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="10796-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="10796-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="10796-113">To polecenie pobiera wszystkie wirtualne sieci WAN, zaczynając od "testu".</span><span class="sxs-lookup"><span data-stu-id="10796-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="10796-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10796-114">PARAMETERS</span></span>

### <span data-ttu-id="10796-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10796-115">-DefaultProfile</span></span>
<span data-ttu-id="10796-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10796-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10796-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10796-117">-Name</span></span>
<span data-ttu-id="10796-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="10796-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="10796-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10796-119">-ResourceGroupName</span></span>
<span data-ttu-id="10796-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10796-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="10796-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10796-121">CommonParameters</span></span>
<span data-ttu-id="10796-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10796-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10796-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10796-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10796-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10796-124">INPUTS</span></span>

### <span data-ttu-id="10796-125">Brak</span><span class="sxs-lookup"><span data-stu-id="10796-125">None</span></span>

## <span data-ttu-id="10796-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10796-126">OUTPUTS</span></span>

### <span data-ttu-id="10796-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="10796-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="10796-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10796-128">NOTES</span></span>

## <span data-ttu-id="10796-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10796-129">RELATED LINKS</span></span>

[<span data-ttu-id="10796-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="10796-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="10796-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="10796-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="10796-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="10796-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
