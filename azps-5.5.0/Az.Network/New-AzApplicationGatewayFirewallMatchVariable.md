---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202962"
---
# <span data-ttu-id="8d81b-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="8d81b-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="8d81b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d81b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d81b-103">Tworzy zmienną dopasowania dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="8d81b-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="8d81b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d81b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d81b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d81b-105">DESCRIPTION</span></span>
<span data-ttu-id="8d81b-106">**New-AzApplicationGatewayFirewallMatchVariable** tworzy zmienną dopasowania dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="8d81b-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="8d81b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d81b-107">EXAMPLES</span></span>

### <span data-ttu-id="8d81b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d81b-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="8d81b-109">Polecenie tworzy nową zmienną dopasowania z nazwami nagłówków żądań, a selektor to pole Content-Length (Długość zawartości).</span><span class="sxs-lookup"><span data-stu-id="8d81b-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="8d81b-110">Nowa zmienna dopasowania jest zapisywana w $variable.</span><span class="sxs-lookup"><span data-stu-id="8d81b-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="8d81b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d81b-111">PARAMETERS</span></span>

### <span data-ttu-id="8d81b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d81b-112">-DefaultProfile</span></span>
<span data-ttu-id="8d81b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d81b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d81b-114">— Selektor</span><span class="sxs-lookup"><span data-stu-id="8d81b-114">-Selector</span></span>
<span data-ttu-id="8d81b-115">W tym artykule opisano pole kolekcji matchVariable.</span><span class="sxs-lookup"><span data-stu-id="8d81b-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="8d81b-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="8d81b-116">-VariableName</span></span>
<span data-ttu-id="8d81b-117">Dopasuj zmienną.</span><span class="sxs-lookup"><span data-stu-id="8d81b-117">Match Variable.</span></span>

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

### <span data-ttu-id="8d81b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d81b-118">CommonParameters</span></span>
<span data-ttu-id="8d81b-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d81b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d81b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d81b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d81b-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d81b-121">INPUTS</span></span>

### <span data-ttu-id="8d81b-122">Brak</span><span class="sxs-lookup"><span data-stu-id="8d81b-122">None</span></span>

## <span data-ttu-id="8d81b-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d81b-123">OUTPUTS</span></span>

### <span data-ttu-id="8d81b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="8d81b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="8d81b-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d81b-125">NOTES</span></span>

## <span data-ttu-id="8d81b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d81b-126">RELATED LINKS</span></span>
