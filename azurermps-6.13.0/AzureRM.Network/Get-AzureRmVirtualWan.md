---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543744"
---
# <span data-ttu-id="86d6e-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="86d6e-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="86d6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="86d6e-103">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="86d6e-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86d6e-104">SYNTAX</span></span>

### <span data-ttu-id="86d6e-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86d6e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86d6e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d6e-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86d6e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="86d6e-107">DESCRIPTION</span></span>
<span data-ttu-id="86d6e-108">Pobiera wirtualną sieć WAN lub wszystkie wirtualne sieci WAN w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="86d6e-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="86d6e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86d6e-109">EXAMPLES</span></span>

### <span data-ttu-id="86d6e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86d6e-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="86d6e-111">To polecenie pobiera wirtualną sieć WAN o nazwie myVirtualWAN w testRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86d6e-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="86d6e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86d6e-112">PARAMETERS</span></span>

### <span data-ttu-id="86d6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d6e-113">-DefaultProfile</span></span>
<span data-ttu-id="86d6e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86d6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d6e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86d6e-115">-Name</span></span>
<span data-ttu-id="86d6e-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="86d6e-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="86d6e-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86d6e-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d6e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d6e-119">CommonParameters</span></span>
<span data-ttu-id="86d6e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d6e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d6e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d6e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d6e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86d6e-122">INPUTS</span></span>

### <span data-ttu-id="86d6e-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="86d6e-123">None</span></span>

## <span data-ttu-id="86d6e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86d6e-124">OUTPUTS</span></span>

### <span data-ttu-id="86d6e-125">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="86d6e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="86d6e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86d6e-126">NOTES</span></span>

## <span data-ttu-id="86d6e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86d6e-127">RELATED LINKS</span></span>
