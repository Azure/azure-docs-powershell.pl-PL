---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 652583ff4425c0403440856a32be3b8107d771ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870283"
---
# <span data-ttu-id="5b7f5-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5b7f5-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="5b7f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7f5-103">Pobiera zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="5b7f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b7f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b7f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b7f5-105">DESCRIPTION</span></span>
<span data-ttu-id="5b7f5-106">Polecenie cmdlet **Get-AzApplicationGatewayFirewallPolicy** pobiera zasady zapory Application Gateway..</span><span class="sxs-lookup"><span data-stu-id="5b7f5-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="5b7f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b7f5-107">EXAMPLES</span></span>

### <span data-ttu-id="5b7f5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b7f5-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5b7f5-109">To polecenie pobiera zasady zapory bramy aplikacji o nazwie FirewallPolicy1 należące do grupy zasobów o nazwie ResourceGroup01 i zapisuje je w zmiennej $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="5b7f5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b7f5-110">PARAMETERS</span></span>

### <span data-ttu-id="5b7f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7f5-111">-DefaultProfile</span></span>
<span data-ttu-id="5b7f5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b7f5-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b7f5-113">-Name</span></span>
<span data-ttu-id="5b7f5-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-114">The resource name.</span></span>

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

### <span data-ttu-id="5b7f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b7f5-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-116">The resource group name.</span></span>

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

### <span data-ttu-id="5b7f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7f5-117">CommonParameters</span></span>
<span data-ttu-id="5b7f5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7f5-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b7f5-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7f5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b7f5-120">INPUTS</span></span>

### <span data-ttu-id="5b7f5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5b7f5-121">System.String</span></span>

## <span data-ttu-id="5b7f5-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b7f5-122">OUTPUTS</span></span>

### <span data-ttu-id="5b7f5-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5b7f5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="5b7f5-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b7f5-124">NOTES</span></span>

## <span data-ttu-id="5b7f5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b7f5-125">RELATED LINKS</span></span>
