---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015066"
---
# <span data-ttu-id="e6ce0-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e6ce0-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e6ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ce0-103">Tworzy zmienną dopasowania dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e6ce0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6ce0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ce0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ce0-106">**New-AzApplicationGatewayFirewallMatchVariable** tworzy zmienną dopasowania dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e6ce0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ce0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6ce0-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="e6ce0-109">Polecenie tworzy nową zmienną dopasowania z nazwami nagłówków żądań, a selektor to pole Content-Length (Długość zawartości).</span><span class="sxs-lookup"><span data-stu-id="e6ce0-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="e6ce0-110">Nowa zmienna dopasowania jest zapisywana w $variable.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="e6ce0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ce0-111">PARAMETERS</span></span>

### <span data-ttu-id="e6ce0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ce0-112">-DefaultProfile</span></span>
<span data-ttu-id="e6ce0-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ce0-114">— Selektor</span><span class="sxs-lookup"><span data-stu-id="e6ce0-114">-Selector</span></span>
<span data-ttu-id="e6ce0-115">W tym artykule opisano pole kolekcji matchVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce0-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="e6ce0-116">-VariableName</span></span>
<span data-ttu-id="e6ce0-117">Dopasuj zmienną.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ce0-118">CommonParameters</span></span>
<span data-ttu-id="e6ce0-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ce0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ce0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ce0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ce0-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6ce0-121">INPUTS</span></span>

### <span data-ttu-id="e6ce0-122">Brak</span><span class="sxs-lookup"><span data-stu-id="e6ce0-122">None</span></span>

## <span data-ttu-id="e6ce0-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6ce0-123">OUTPUTS</span></span>

### <span data-ttu-id="e6ce0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e6ce0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e6ce0-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6ce0-125">NOTES</span></span>

## <span data-ttu-id="e6ce0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6ce0-126">RELATED LINKS</span></span>
