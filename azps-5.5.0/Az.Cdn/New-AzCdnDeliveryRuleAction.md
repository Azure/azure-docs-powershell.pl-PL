---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177874"
---
# <span data-ttu-id="c2427-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="c2427-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="c2427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2427-102">SYNOPSIS</span></span>
<span data-ttu-id="c2427-103">Tworzy akcję dostarczania.</span><span class="sxs-lookup"><span data-stu-id="c2427-103">Creates a delivery action.</span></span>

## <span data-ttu-id="c2427-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2427-104">SYNTAX</span></span>

### <span data-ttu-id="c2427-105">CacheExpirationActionParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c2427-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2427-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2427-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2427-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2427-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2427-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2427-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2427-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2427-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2427-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2427-110">DESCRIPTION</span></span>
<span data-ttu-id="c2427-111">Polecenie **cmdlet New-AzCdnDeliveryRule** tworzy regułę dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c2427-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="c2427-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2427-112">EXAMPLES</span></span>

### <span data-ttu-id="c2427-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2427-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="c2427-114">Utwórz prostą regułę dostarczania.</span><span class="sxs-lookup"><span data-stu-id="c2427-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="c2427-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2427-115">PARAMETERS</span></span>

### <span data-ttu-id="c2427-116">— Akcja</span><span class="sxs-lookup"><span data-stu-id="c2427-116">-Action</span></span>
<span data-ttu-id="c2427-117">Akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="c2427-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-118">- CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="c2427-118">-CacheBehavior</span></span>
<span data-ttu-id="c2427-119">Zachowanie buforowania dla akcji</span><span class="sxs-lookup"><span data-stu-id="c2427-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="c2427-120">-CacheDuration</span></span>
<span data-ttu-id="c2427-121">Czas trwania, przez jaki zawartość musi być buforowana.</span><span class="sxs-lookup"><span data-stu-id="c2427-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="c2427-122">Dozwolony format \[ to d. \] gg:mm:ss</span><span class="sxs-lookup"><span data-stu-id="c2427-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-123">- CustomFragment</span><span class="sxs-lookup"><span data-stu-id="c2427-123">-CustomFragment</span></span>
<span data-ttu-id="c2427-124">Fragment, aby dodać do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="c2427-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="c2427-125">Fragment to część adresu URL, która pojawia się po #.</span><span class="sxs-lookup"><span data-stu-id="c2427-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="c2427-126">Nie dołączaj błędu #.</span><span class="sxs-lookup"><span data-stu-id="c2427-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="c2427-127">-CustomHostname</span></span>
<span data-ttu-id="c2427-128">Host, aby przekierować.</span><span class="sxs-lookup"><span data-stu-id="c2427-128">Host to redirect.</span></span>
<span data-ttu-id="c2427-129">Pozostaw puste, aby użyć hosta poczty przychodzącej jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="c2427-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-130">— CustomPath</span><span class="sxs-lookup"><span data-stu-id="c2427-130">-CustomPath</span></span>
<span data-ttu-id="c2427-131">Pełna ścieżka przekierowania.</span><span class="sxs-lookup"><span data-stu-id="c2427-131">The full path to redirect.</span></span>
<span data-ttu-id="c2427-132">Ścieżka nie może być pusta i musi zaczynać się od /.</span><span class="sxs-lookup"><span data-stu-id="c2427-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="c2427-133">Pozostaw puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="c2427-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-134">- CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="c2427-134">-CustomQueryString</span></span>
<span data-ttu-id="c2427-135">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="c2427-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="c2427-136">Ustawienie tej wartości zastąpi wszelkie istniejące ciągi zapytania. pozostaw puste, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="c2427-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="c2427-137">Ciąg zapytania musi mieć \<key\> = \<value\> format.</span><span class="sxs-lookup"><span data-stu-id="c2427-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="c2427-138">?</span><span class="sxs-lookup"><span data-stu-id="c2427-138">?</span></span> <span data-ttu-id="c2427-139">i & zostaną dodane automatycznie, więc ich nie dołączaj.</span><span class="sxs-lookup"><span data-stu-id="c2427-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2427-140">-DefaultProfile</span></span>
<span data-ttu-id="c2427-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2427-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2427-142">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="c2427-142">-Destination</span></span>
<span data-ttu-id="c2427-143">Zdefiniuj względny adres URL, według którego zostaną napisane ponownie powyższe żądania.</span><span class="sxs-lookup"><span data-stu-id="c2427-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="c2427-144">-DestinationProtocol</span></span>
<span data-ttu-id="c2427-145">Protokół używany do przekierowywania.</span><span class="sxs-lookup"><span data-stu-id="c2427-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="c2427-146">Wartość domyślna to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="c2427-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="c2427-147">-HeaderActionType</span></span>
<span data-ttu-id="c2427-148">Czy zmodyfikować nagłówek żądania lub nagłówek odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="c2427-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c2427-149">-HeaderName</span></span>
<span data-ttu-id="c2427-150">Nazwa nagłówka do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="c2427-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-151">- PreservePath</span><span class="sxs-lookup"><span data-stu-id="c2427-151">-PreservePath</span></span>
<span data-ttu-id="c2427-152">Czy zachowywać niepasową ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="c2427-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-153">-QueryParameters</span><span class="sxs-lookup"><span data-stu-id="c2427-153">-QueryParameter</span></span>
<span data-ttu-id="c2427-154">Parametry kwerendy dołączane lub wykluczane (rozdzielane przecinkami).</span><span class="sxs-lookup"><span data-stu-id="c2427-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="c2427-155">-QueryStringBehavior</span></span>
<span data-ttu-id="c2427-156">Zachowanie ciągu zapytania dla żądań</span><span class="sxs-lookup"><span data-stu-id="c2427-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c2427-157">-RedirectType</span></span>
<span data-ttu-id="c2427-158">Podczas przekierowywania ruchu użyje ona typu przekierowywania</span><span class="sxs-lookup"><span data-stu-id="c2427-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="c2427-159">-SourcePattern</span></span>
<span data-ttu-id="c2427-160">Zdefiniuj wzorzec identyfikatorów URI żądania identyfikujący typ żądań, które mogą być pisane ponownie.</span><span class="sxs-lookup"><span data-stu-id="c2427-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="c2427-161">Jeśli wartość jest pusta, zostaną dopasowane wszystkie ciągi.</span><span class="sxs-lookup"><span data-stu-id="c2427-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-162">— Wartość</span><span class="sxs-lookup"><span data-stu-id="c2427-162">-Value</span></span>
<span data-ttu-id="c2427-163">Wartość określonej akcji.</span><span class="sxs-lookup"><span data-stu-id="c2427-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2427-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2427-164">CommonParameters</span></span>
<span data-ttu-id="c2427-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2427-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2427-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2427-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2427-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2427-167">INPUTS</span></span>

### <span data-ttu-id="c2427-168">Brak</span><span class="sxs-lookup"><span data-stu-id="c2427-168">None</span></span>

## <span data-ttu-id="c2427-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2427-169">OUTPUTS</span></span>

### <span data-ttu-id="c2427-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="c2427-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="c2427-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2427-171">NOTES</span></span>

## <span data-ttu-id="c2427-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2427-172">RELATED LINKS</span></span>
