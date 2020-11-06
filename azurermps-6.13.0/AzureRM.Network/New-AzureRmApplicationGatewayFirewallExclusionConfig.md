---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547472"
---
# <span data-ttu-id="31182-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="31182-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="31182-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31182-102">SYNOPSIS</span></span>
<span data-ttu-id="31182-103">Tworzy nową listę reguł wykluczeń dla usługi Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="31182-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31182-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31182-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31182-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31182-105">DESCRIPTION</span></span>
<span data-ttu-id="31182-106">Polecenie cmdlet **New-AzureRmApplicationGatewayFirewallExclusionConfig** z listą reguł wykluczeń dla bramy Application WAF.</span><span class="sxs-lookup"><span data-stu-id="31182-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="31182-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31182-107">EXAMPLES</span></span>

### <span data-ttu-id="31182-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31182-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="31182-109">To polecenie tworzy nową konfigurację listy reguł wykluczeń dla zmiennej o nazwie RequestHeaderNames oraz operatora o nazwie StartsWith i selektora o nazwie xyz.</span><span class="sxs-lookup"><span data-stu-id="31182-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="31182-110">Konfiguracja listy wykluczeń jest zapisywana w $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="31182-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="31182-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31182-111">PARAMETERS</span></span>

### <span data-ttu-id="31182-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31182-112">-DefaultProfile</span></span>
<span data-ttu-id="31182-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31182-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31182-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="31182-114">-Operator</span></span>
<span data-ttu-id="31182-115">Gdy zmienna jest kolekcją, działa na selektorze w celu określenia, których elementów w kolekcji dotyczy wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="31182-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="31182-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="31182-116">-Selector</span></span>
<span data-ttu-id="31182-117">Gdy zmienna jest kolekcją, operator służy do określenia, do których elementów w kolekcji odnosi się wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="31182-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="31182-118">-Zmienna</span><span class="sxs-lookup"><span data-stu-id="31182-118">-Variable</span></span>
<span data-ttu-id="31182-119">Zmienna, którą należy wykluczyć.</span><span class="sxs-lookup"><span data-stu-id="31182-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="31182-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31182-120">CommonParameters</span></span>
<span data-ttu-id="31182-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31182-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31182-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31182-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31182-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31182-123">INPUTS</span></span>

### <span data-ttu-id="31182-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="31182-124">None</span></span>

## <span data-ttu-id="31182-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31182-125">OUTPUTS</span></span>

### <span data-ttu-id="31182-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="31182-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="31182-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31182-127">NOTES</span></span>

## <span data-ttu-id="31182-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31182-128">RELATED LINKS</span></span>
