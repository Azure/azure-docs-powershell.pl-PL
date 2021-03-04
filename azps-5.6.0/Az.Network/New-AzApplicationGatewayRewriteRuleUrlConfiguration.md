---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952186"
---
# <span data-ttu-id="b8eba-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8eba-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="b8eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8eba-102">SYNOPSIS</span></span>
<span data-ttu-id="b8eba-103">Tworzy konfigurację adresu URL reguły ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b8eba-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="b8eba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8eba-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8eba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8eba-105">DESCRIPTION</span></span>
<span data-ttu-id="b8eba-106">**Polecenie cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** tworzy konfigurację adresu URL reguły ponownego w przypadku bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="b8eba-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="b8eba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8eba-107">EXAMPLES</span></span>

### <span data-ttu-id="b8eba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8eba-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="b8eba-109">To polecenie tworzy konfigurację adresu URL reguły ponownego tworzenia i zapisuje wynik w zmiennej o nazwie $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8eba-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="b8eba-110">Jeśli chcesz zaktualizować istniejącą konfigurację adresu URL, możesz to zrobić, tworząc nową konfigurację UrlConfiguration i przypisując nową właściwość UrlConfiguration do właściwości UrlConfiguration zestawu akcji Przepisz regułę.</span><span class="sxs-lookup"><span data-stu-id="b8eba-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="b8eba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8eba-111">PARAMETERS</span></span>

### <span data-ttu-id="b8eba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8eba-112">-DefaultProfile</span></span>
<span data-ttu-id="b8eba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8eba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8eba-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="b8eba-114">-ModifiedPath</span></span>
<span data-ttu-id="b8eba-115">Wartość ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="b8eba-115">Url path value.</span></span>

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

### <span data-ttu-id="b8eba-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="b8eba-116">-ModifiedQueryString</span></span>
<span data-ttu-id="b8eba-117">Wartość ciągu zapytania adresu URL.</span><span class="sxs-lookup"><span data-stu-id="b8eba-117">Url query string value.</span></span>

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

### <span data-ttu-id="b8eba-118">— Przekieruj</span><span class="sxs-lookup"><span data-stu-id="b8eba-118">-Reroute</span></span>
<span data-ttu-id="b8eba-119">Flaga w celu ponownego oceny mapy ścieżki adresu URL dostępnej w zasadach routingu opartych na ścieżkach żądań przy użyciu zmodyfikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="b8eba-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8eba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8eba-120">CommonParameters</span></span>
<span data-ttu-id="b8eba-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8eba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8eba-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8eba-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8eba-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8eba-123">INPUTS</span></span>

### <span data-ttu-id="b8eba-124">Brak</span><span class="sxs-lookup"><span data-stu-id="b8eba-124">None</span></span>

## <span data-ttu-id="b8eba-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8eba-125">OUTPUTS</span></span>

### <span data-ttu-id="b8eba-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8eba-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="b8eba-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8eba-127">NOTES</span></span>

## <span data-ttu-id="b8eba-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8eba-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8eba-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b8eba-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b8eba-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b8eba-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b8eba-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b8eba-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b8eba-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b8eba-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b8eba-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)