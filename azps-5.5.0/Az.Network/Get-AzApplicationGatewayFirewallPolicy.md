---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179931"
---
# <span data-ttu-id="b76d0-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b76d0-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="b76d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b76d0-103">Pobiera zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b76d0-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="b76d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b76d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76d0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b76d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b76d0-106">Polecenie **cmdlet Get-AzApplicationGatewayFirewallPolicy** otrzymuje zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b76d0-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="b76d0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b76d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b76d0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b76d0-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b76d0-109">To polecenie pobiera zasady zapory bramy aplikacji o nazwie FirewallPolicy1, które należą do grupy zasobów o nazwie ResourceGroup01, i przechowuje je w zmiennej $AppGwFirewallPolicy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b76d0-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="b76d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b76d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76d0-111">-DefaultProfile</span></span>
<span data-ttu-id="b76d0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b76d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76d0-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b76d0-113">-Name</span></span>
<span data-ttu-id="b76d0-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b76d0-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76d0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76d0-115">-ResourceGroupName</span></span>
<span data-ttu-id="b76d0-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b76d0-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76d0-117">CommonParameters</span></span>
<span data-ttu-id="b76d0-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76d0-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b76d0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76d0-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b76d0-120">INPUTS</span></span>

### <span data-ttu-id="b76d0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b76d0-121">System.String</span></span>

## <span data-ttu-id="b76d0-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b76d0-122">OUTPUTS</span></span>

### <span data-ttu-id="b76d0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b76d0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b76d0-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b76d0-124">NOTES</span></span>

## <span data-ttu-id="b76d0-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b76d0-125">RELATED LINKS</span></span>
