---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223108"
---
# <span data-ttu-id="cd64c-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cd64c-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="cd64c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd64c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd64c-103">Pobiera zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd64c-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="cd64c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd64c-104">SYNTAX</span></span>

### <span data-ttu-id="cd64c-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd64c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd64c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd64c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd64c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd64c-107">DESCRIPTION</span></span>
<span data-ttu-id="cd64c-108">Polecenie cmdlet **Get-AzFirewallPolicy** pobiera co najmniej jedno okno zapory w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="cd64c-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="cd64c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd64c-109">EXAMPLES</span></span>

### <span data-ttu-id="cd64c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd64c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="cd64c-111">W tym przykładzie otrzymano zasady zapory o nazwie "firewallPolicy" w grupie zasobów "TestRg".</span><span class="sxs-lookup"><span data-stu-id="cd64c-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="cd64c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd64c-112">PARAMETERS</span></span>

### <span data-ttu-id="cd64c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd64c-113">-DefaultProfile</span></span>
<span data-ttu-id="cd64c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd64c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd64c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd64c-115">-Name</span></span>
<span data-ttu-id="cd64c-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cd64c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd64c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd64c-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd64c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd64c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd64c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd64c-119">-ResourceId</span></span>
<span data-ttu-id="cd64c-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cd64c-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd64c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd64c-121">CommonParameters</span></span>
<span data-ttu-id="cd64c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd64c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd64c-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd64c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd64c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd64c-124">INPUTS</span></span>

### <span data-ttu-id="cd64c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cd64c-125">System.String</span></span>

## <span data-ttu-id="cd64c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd64c-126">OUTPUTS</span></span>

### <span data-ttu-id="cd64c-127">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="cd64c-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="cd64c-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd64c-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cd64c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd64c-129">NOTES</span></span>

## <span data-ttu-id="cd64c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd64c-130">RELATED LINKS</span></span>
