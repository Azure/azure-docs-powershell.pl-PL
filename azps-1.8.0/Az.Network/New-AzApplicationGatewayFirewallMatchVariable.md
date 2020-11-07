---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 05a1929f79799be8006ae82c4948dc0a81839040
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709380"
---
# <span data-ttu-id="ceb68-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="ceb68-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="ceb68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ceb68-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb68-103">Tworzy zmienną dopasowania dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="ceb68-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="ceb68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ceb68-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb68-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ceb68-105">DESCRIPTION</span></span>
<span data-ttu-id="ceb68-106">**Nowy — AzApplicationGatewayFirewallMatchVariable** tworzy zmienną Match dla warunku zapory.</span><span class="sxs-lookup"><span data-stu-id="ceb68-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="ceb68-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ceb68-107">EXAMPLES</span></span>

### <span data-ttu-id="ceb68-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ceb68-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzureRmApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="ceb68-109">Polecenie tworzy nową zmienną dopasowania z nazwą nagłówków żądania i selektorem jest pole Content-Length.</span><span class="sxs-lookup"><span data-stu-id="ceb68-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="ceb68-110">Nowa zmienna dopasowania jest zapisywana w $variable.</span><span class="sxs-lookup"><span data-stu-id="ceb68-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="ceb68-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ceb68-111">PARAMETERS</span></span>

### <span data-ttu-id="ceb68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb68-112">-DefaultProfile</span></span>
<span data-ttu-id="ceb68-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb68-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb68-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="ceb68-114">-Selector</span></span>
<span data-ttu-id="ceb68-115">Opis pola kolekcji matchVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb68-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="ceb68-116">-Zmiennaname</span><span class="sxs-lookup"><span data-stu-id="ceb68-116">-VariableName</span></span>
<span data-ttu-id="ceb68-117">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ceb68-117">Match Variable.</span></span>

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

### <span data-ttu-id="ceb68-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb68-118">CommonParameters</span></span>
<span data-ttu-id="ceb68-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb68-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb68-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb68-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb68-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceb68-121">INPUTS</span></span>

### <span data-ttu-id="ceb68-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ceb68-122">None</span></span>

## <span data-ttu-id="ceb68-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ceb68-123">OUTPUTS</span></span>

### <span data-ttu-id="ceb68-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="ceb68-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="ceb68-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ceb68-125">NOTES</span></span>

## <span data-ttu-id="ceb68-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceb68-126">RELATED LINKS</span></span>