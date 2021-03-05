---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 029ba60169ee22d86d9e54661296f04bf2242713
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964202"
---
# <span data-ttu-id="8e33a-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="8e33a-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="8e33a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e33a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e33a-103">Tworzy nową listę reguł wykluczeń dla nieaf bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8e33a-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="8e33a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e33a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e33a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e33a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e33a-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallExclusionConfig** nowej listy reguł wykluczeń dla bramy aplikacji nieaf.</span><span class="sxs-lookup"><span data-stu-id="8e33a-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="8e33a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e33a-107">EXAMPLES</span></span>

### <span data-ttu-id="8e33a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e33a-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="8e33a-109">To polecenie tworzy nową regułę wykluczeń dla zmiennej o nazwach RequestHeaderNames i operatora StartsWith oraz Selektor o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="8e33a-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="8e33a-110">Konfiguracja listy wykluczeń jest zapisywana w $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="8e33a-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="8e33a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e33a-111">PARAMETERS</span></span>

### <span data-ttu-id="8e33a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e33a-112">-DefaultProfile</span></span>
<span data-ttu-id="8e33a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e33a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e33a-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="8e33a-114">-Operator</span></span>
<span data-ttu-id="8e33a-115">Jeśli zmienna jest kolekcją, operuj na selektorze, aby określić, których elementów w kolekcji dotyczy to wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="8e33a-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e33a-116">— Selektor</span><span class="sxs-lookup"><span data-stu-id="8e33a-116">-Selector</span></span>
<span data-ttu-id="8e33a-117">Jeśli zmienna jest kolekcją, operator używany do określania elementów w kolekcji, których dotyczy to wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="8e33a-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e33a-118">—Zmienna</span><span class="sxs-lookup"><span data-stu-id="8e33a-118">-Variable</span></span>
<span data-ttu-id="8e33a-119">Zmienna do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="8e33a-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e33a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e33a-120">CommonParameters</span></span>
<span data-ttu-id="8e33a-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e33a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e33a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e33a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e33a-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e33a-123">INPUTS</span></span>

### <span data-ttu-id="8e33a-124">Brak</span><span class="sxs-lookup"><span data-stu-id="8e33a-124">None</span></span>

## <span data-ttu-id="8e33a-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e33a-125">OUTPUTS</span></span>

### <span data-ttu-id="8e33a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="8e33a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="8e33a-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e33a-127">NOTES</span></span>

## <span data-ttu-id="8e33a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e33a-128">RELATED LINKS</span></span>
