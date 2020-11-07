---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: 107f2b7b41143c2f121b358eaf29c99537f51a69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709428"
---
# <span data-ttu-id="064ac-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="064ac-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="064ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="064ac-102">SYNOPSIS</span></span>
<span data-ttu-id="064ac-103">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="064ac-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="064ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="064ac-104">SYNTAX</span></span>

### <span data-ttu-id="064ac-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="064ac-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="064ac-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064ac-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="064ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="064ac-107">DESCRIPTION</span></span>
<span data-ttu-id="064ac-108">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="064ac-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="064ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="064ac-109">EXAMPLES</span></span>

### <span data-ttu-id="064ac-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="064ac-110">Example 1</span></span>

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

<span data-ttu-id="064ac-111">To polecenie pobiera wirtualną sieć WAN o nazwie myVirtualWAN w testRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="064ac-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="064ac-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="064ac-112">Example 2</span></span>

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

<span data-ttu-id="064ac-113">To polecenie pobiera wszystkie wirtualne sieci WAN, rozpoczynając od "test".</span><span class="sxs-lookup"><span data-stu-id="064ac-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="064ac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="064ac-114">PARAMETERS</span></span>

### <span data-ttu-id="064ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064ac-115">-DefaultProfile</span></span>
<span data-ttu-id="064ac-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="064ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064ac-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="064ac-117">-Name</span></span>
<span data-ttu-id="064ac-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="064ac-118">The resource name.</span></span>

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

### <span data-ttu-id="064ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="064ac-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="064ac-120">The resource group name.</span></span>

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

### <span data-ttu-id="064ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064ac-121">CommonParameters</span></span>
<span data-ttu-id="064ac-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064ac-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="064ac-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064ac-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="064ac-124">INPUTS</span></span>

### <span data-ttu-id="064ac-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="064ac-125">None</span></span>

## <span data-ttu-id="064ac-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="064ac-126">OUTPUTS</span></span>

### <span data-ttu-id="064ac-127">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="064ac-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="064ac-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="064ac-128">NOTES</span></span>

## <span data-ttu-id="064ac-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="064ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="064ac-130">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="064ac-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="064ac-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="064ac-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="064ac-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="064ac-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)