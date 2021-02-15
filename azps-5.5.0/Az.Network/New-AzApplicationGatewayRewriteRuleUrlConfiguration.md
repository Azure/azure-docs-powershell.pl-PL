---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187107"
---
# <span data-ttu-id="96eef-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="96eef-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="96eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96eef-102">SYNOPSIS</span></span>
<span data-ttu-id="96eef-103">Tworzy konfigurację adresu URL reguły ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="96eef-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="96eef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96eef-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96eef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="96eef-105">DESCRIPTION</span></span>
<span data-ttu-id="96eef-106">**Polecenie cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** tworzy konfigurację adresu URL reguły ponownego w przypadku bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="96eef-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="96eef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96eef-107">EXAMPLES</span></span>

### <span data-ttu-id="96eef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96eef-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="96eef-109">To polecenie tworzy konfigurację adresu URL reguły ponownego tworzenia i zapisuje wynik w zmiennej o nazwie $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="96eef-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="96eef-110">Jeśli chcesz zaktualizować dowolną istniejącą konfigurację url, możesz to zrobić, tworząc nową konfigurację UrlConfiguration i przypisując nową właściwość UrlConfiguration do właściwości UrlConfiguration zestawu akcji Przepisz regułę.</span><span class="sxs-lookup"><span data-stu-id="96eef-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="96eef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96eef-111">PARAMETERS</span></span>

### <span data-ttu-id="96eef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96eef-112">-DefaultProfile</span></span>
<span data-ttu-id="96eef-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96eef-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96eef-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="96eef-114">-ModifiedPath</span></span>
<span data-ttu-id="96eef-115">Wartość ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="96eef-115">Url path value.</span></span>

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

### <span data-ttu-id="96eef-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="96eef-116">-ModifiedQueryString</span></span>
<span data-ttu-id="96eef-117">Wartość ciągu zapytania adresu URL.</span><span class="sxs-lookup"><span data-stu-id="96eef-117">Url query string value.</span></span>

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

### <span data-ttu-id="96eef-118">— Przekieruj</span><span class="sxs-lookup"><span data-stu-id="96eef-118">-Reroute</span></span>
<span data-ttu-id="96eef-119">Flaga w celu ponownego oceny mapy ścieżki adresu URL dostępnej w zasadach routingu opartych na ścieżkach żądań przy użyciu zmodyfikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="96eef-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="96eef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96eef-120">CommonParameters</span></span>
<span data-ttu-id="96eef-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96eef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96eef-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96eef-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96eef-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96eef-123">INPUTS</span></span>

### <span data-ttu-id="96eef-124">Brak</span><span class="sxs-lookup"><span data-stu-id="96eef-124">None</span></span>

## <span data-ttu-id="96eef-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96eef-125">OUTPUTS</span></span>

### <span data-ttu-id="96eef-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="96eef-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="96eef-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96eef-127">NOTES</span></span>

## <span data-ttu-id="96eef-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96eef-128">RELATED LINKS</span></span>

[<span data-ttu-id="96eef-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96eef-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96eef-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96eef-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96eef-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96eef-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96eef-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96eef-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96eef-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96eef-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96eef-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="96eef-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="96eef-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="96eef-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)