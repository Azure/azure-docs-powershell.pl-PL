---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: 127c73a34b030a991b5875f141ea8dd850a4f0a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009249"
---
# <span data-ttu-id="af222-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="af222-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="af222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af222-102">SYNOPSIS</span></span>
<span data-ttu-id="af222-103">Tworzy akcję dostarczania.</span><span class="sxs-lookup"><span data-stu-id="af222-103">Creates a delivery action.</span></span>

## <span data-ttu-id="af222-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af222-104">SYNTAX</span></span>

### <span data-ttu-id="af222-105">CacheExpirationActionParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="af222-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af222-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="af222-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af222-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="af222-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af222-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="af222-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af222-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="af222-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af222-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="af222-110">DESCRIPTION</span></span>
<span data-ttu-id="af222-111">Polecenie **cmdlet New-AzCdnDeliveryRule** tworzy regułę dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="af222-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="af222-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af222-112">EXAMPLES</span></span>

### <span data-ttu-id="af222-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af222-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="af222-114">Utwórz prostą regułę dostarczania.</span><span class="sxs-lookup"><span data-stu-id="af222-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="af222-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af222-115">PARAMETERS</span></span>

### <span data-ttu-id="af222-116">— Akcja</span><span class="sxs-lookup"><span data-stu-id="af222-116">-Action</span></span>
<span data-ttu-id="af222-117">Akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="af222-117">Action to perform.</span></span>

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

### <span data-ttu-id="af222-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="af222-118">-CacheBehavior</span></span>
<span data-ttu-id="af222-119">Zachowanie buforowania dla akcji</span><span class="sxs-lookup"><span data-stu-id="af222-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="af222-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="af222-120">-CacheDuration</span></span>
<span data-ttu-id="af222-121">Czas trwania, przez który zawartość musi być buforowana.</span><span class="sxs-lookup"><span data-stu-id="af222-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="af222-122">Dozwolony format \[ to d. \] gg:mm:ss</span><span class="sxs-lookup"><span data-stu-id="af222-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="af222-123">- CustomFragment</span><span class="sxs-lookup"><span data-stu-id="af222-123">-CustomFragment</span></span>
<span data-ttu-id="af222-124">Fragment, który należy dodać do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="af222-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="af222-125">Fragment to część adresu URL, która pojawia się po #.</span><span class="sxs-lookup"><span data-stu-id="af222-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="af222-126">Nie dołączaj błędu #.</span><span class="sxs-lookup"><span data-stu-id="af222-126">Do not include the #.</span></span>

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

### <span data-ttu-id="af222-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="af222-127">-CustomHostname</span></span>
<span data-ttu-id="af222-128">Host, aby przekierować.</span><span class="sxs-lookup"><span data-stu-id="af222-128">Host to redirect.</span></span>
<span data-ttu-id="af222-129">Pozostaw puste, aby użyć hosta poczty przychodzącej jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="af222-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="af222-130">— CustomPath</span><span class="sxs-lookup"><span data-stu-id="af222-130">-CustomPath</span></span>
<span data-ttu-id="af222-131">Pełna ścieżka przekierowania.</span><span class="sxs-lookup"><span data-stu-id="af222-131">The full path to redirect.</span></span>
<span data-ttu-id="af222-132">Ścieżka nie może być pusta i musi zaczynać się od /.</span><span class="sxs-lookup"><span data-stu-id="af222-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="af222-133">Pozostaw puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="af222-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="af222-134">- CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="af222-134">-CustomQueryString</span></span>
<span data-ttu-id="af222-135">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="af222-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="af222-136">Ustawienie tej wartości zastąpi wszelkie istniejące ciągi zapytania. pozostaw puste, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="af222-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="af222-137">Ciąg zapytania musi mieć \<key\> = \<value\> format.</span><span class="sxs-lookup"><span data-stu-id="af222-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="af222-138">?</span><span class="sxs-lookup"><span data-stu-id="af222-138">?</span></span> <span data-ttu-id="af222-139">i & zostaną dodane automatycznie, więc ich nie dołączaj.</span><span class="sxs-lookup"><span data-stu-id="af222-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="af222-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af222-140">-DefaultProfile</span></span>
<span data-ttu-id="af222-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="af222-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af222-142">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="af222-142">-Destination</span></span>
<span data-ttu-id="af222-143">Zdefiniuj względny adres URL, według którego zostaną napisane ponownie powyższe żądania.</span><span class="sxs-lookup"><span data-stu-id="af222-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="af222-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="af222-144">-DestinationProtocol</span></span>
<span data-ttu-id="af222-145">Protokół używany do przekierowywania.</span><span class="sxs-lookup"><span data-stu-id="af222-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="af222-146">Wartość domyślna to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="af222-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="af222-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="af222-147">-HeaderActionType</span></span>
<span data-ttu-id="af222-148">Czy zmodyfikować nagłówek żądania lub nagłówek odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="af222-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="af222-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="af222-149">-HeaderName</span></span>
<span data-ttu-id="af222-150">Nazwa nagłówka do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="af222-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="af222-151">- PreservePath</span><span class="sxs-lookup"><span data-stu-id="af222-151">-PreservePath</span></span>
<span data-ttu-id="af222-152">Czy zachowywać niepasową ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="af222-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="af222-153">-QueryParameters</span><span class="sxs-lookup"><span data-stu-id="af222-153">-QueryParameter</span></span>
<span data-ttu-id="af222-154">Parametry kwerendy dołączane lub wykluczane (rozdzielane przecinkami).</span><span class="sxs-lookup"><span data-stu-id="af222-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="af222-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="af222-155">-QueryStringBehavior</span></span>
<span data-ttu-id="af222-156">Zachowanie ciągu zapytania dla żądań</span><span class="sxs-lookup"><span data-stu-id="af222-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="af222-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="af222-157">-RedirectType</span></span>
<span data-ttu-id="af222-158">Typ przekierowywania będzie używać reguły podczas przekierowywania ruchu</span><span class="sxs-lookup"><span data-stu-id="af222-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="af222-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="af222-159">-SourcePattern</span></span>
<span data-ttu-id="af222-160">Zdefiniuj wzorzec identyfikatorów URI żądania identyfikujący typ żądań, które mogą być pisane ponownie.</span><span class="sxs-lookup"><span data-stu-id="af222-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="af222-161">Jeśli wartość jest pusta, zostaną dopasowane wszystkie ciągi.</span><span class="sxs-lookup"><span data-stu-id="af222-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="af222-162">— Wartość</span><span class="sxs-lookup"><span data-stu-id="af222-162">-Value</span></span>
<span data-ttu-id="af222-163">Wartość określonej akcji.</span><span class="sxs-lookup"><span data-stu-id="af222-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="af222-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af222-164">CommonParameters</span></span>
<span data-ttu-id="af222-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af222-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af222-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af222-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af222-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af222-167">INPUTS</span></span>

### <span data-ttu-id="af222-168">Brak</span><span class="sxs-lookup"><span data-stu-id="af222-168">None</span></span>

## <span data-ttu-id="af222-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af222-169">OUTPUTS</span></span>

### <span data-ttu-id="af222-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="af222-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="af222-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af222-171">NOTES</span></span>

## <span data-ttu-id="af222-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af222-172">RELATED LINKS</span></span>
