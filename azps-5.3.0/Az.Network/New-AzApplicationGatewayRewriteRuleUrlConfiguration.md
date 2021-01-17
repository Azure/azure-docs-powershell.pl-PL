---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379318"
---
# <span data-ttu-id="3f61f-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f61f-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="3f61f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f61f-102">SYNOPSIS</span></span>
<span data-ttu-id="3f61f-103">Umożliwia utworzenie konfiguracji adresu URL reguły ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f61f-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="3f61f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f61f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f61f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f61f-105">DESCRIPTION</span></span>
<span data-ttu-id="3f61f-106">Polecenie cmdlet **AzApplicationGatewayRewriteRuleUrlConfiguration** tworzy konfigurację adresu URL reguły ponownej edycji dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f61f-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="3f61f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f61f-107">EXAMPLES</span></span>

### <span data-ttu-id="3f61f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f61f-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="3f61f-109">To polecenie umożliwia utworzenie konfiguracji adresu URL reguły ponownej edycji i zapisanie wyniku w zmiennej o nazwie $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3f61f-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="3f61f-110">Jeśli chcesz zaktualizować wszystkie istniejące UrlConfiguration, możesz to zrobić, tworząc nowy UrlConfiguration i przypisując nowy UrlConfiguration do właściwości UrlConfiguration akcji reguły ponownego zapisu.</span><span class="sxs-lookup"><span data-stu-id="3f61f-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="3f61f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f61f-111">PARAMETERS</span></span>

### <span data-ttu-id="3f61f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f61f-112">-DefaultProfile</span></span>
<span data-ttu-id="3f61f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f61f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f61f-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="3f61f-114">-ModifiedPath</span></span>
<span data-ttu-id="3f61f-115">Wartość ścieżki URL.</span><span class="sxs-lookup"><span data-stu-id="3f61f-115">Url path value.</span></span>

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

### <span data-ttu-id="3f61f-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="3f61f-116">-ModifiedQueryString</span></span>
<span data-ttu-id="3f61f-117">Wartość ciągu kwerendy adresu URL.</span><span class="sxs-lookup"><span data-stu-id="3f61f-117">Url query string value.</span></span>

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

### <span data-ttu-id="3f61f-118">-Przekieruj</span><span class="sxs-lookup"><span data-stu-id="3f61f-118">-Reroute</span></span>
<span data-ttu-id="3f61f-119">Flaga ponownego oszacowania mapy ścieżki adresu URL podanej w regułach przekierowywania żądań opartych na ścieżce przy użyciu zmodyfikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="3f61f-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="3f61f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f61f-120">CommonParameters</span></span>
<span data-ttu-id="3f61f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f61f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f61f-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f61f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f61f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f61f-123">INPUTS</span></span>

### <span data-ttu-id="3f61f-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f61f-124">None</span></span>

## <span data-ttu-id="3f61f-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f61f-125">OUTPUTS</span></span>

### <span data-ttu-id="3f61f-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f61f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="3f61f-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f61f-127">NOTES</span></span>

## <span data-ttu-id="3f61f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f61f-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f61f-129">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f61f-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f61f-131">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f61f-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f61f-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f61f-134">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3f61f-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3f61f-135">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3f61f-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)