---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064292"
---
# <span data-ttu-id="13db5-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="13db5-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="13db5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13db5-102">SYNOPSIS</span></span>
<span data-ttu-id="13db5-103">Umożliwia utworzenie akcji dostarczania.</span><span class="sxs-lookup"><span data-stu-id="13db5-103">Creates a delivery action.</span></span>

## <span data-ttu-id="13db5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13db5-104">SYNTAX</span></span>

### <span data-ttu-id="13db5-105">CacheExpirationActionParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13db5-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13db5-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="13db5-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13db5-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="13db5-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13db5-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="13db5-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13db5-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="13db5-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13db5-110">Opis</span><span class="sxs-lookup"><span data-stu-id="13db5-110">DESCRIPTION</span></span>
<span data-ttu-id="13db5-111">Polecenie cmdlet **New-AzCdnDeliveryRule** umożliwia utworzenie reguły dostarczania dla tworzenia punktu końcowego usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="13db5-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="13db5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13db5-112">EXAMPLES</span></span>

### <span data-ttu-id="13db5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13db5-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="13db5-114">Tworzenie prostej reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="13db5-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="13db5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13db5-115">PARAMETERS</span></span>

### <span data-ttu-id="13db5-116">-Action</span><span class="sxs-lookup"><span data-stu-id="13db5-116">-Action</span></span>
<span data-ttu-id="13db5-117">Akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="13db5-117">Action to perform.</span></span>

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

### <span data-ttu-id="13db5-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="13db5-118">-CacheBehavior</span></span>
<span data-ttu-id="13db5-119">Zachowanie funkcji buforowania dla akcji</span><span class="sxs-lookup"><span data-stu-id="13db5-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="13db5-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="13db5-120">-CacheDuration</span></span>
<span data-ttu-id="13db5-121">Czas trwania, dla którego zawartość musi być buforowana.</span><span class="sxs-lookup"><span data-stu-id="13db5-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="13db5-122">Dozwolony format to \[ d. \] GG: mm: SS</span><span class="sxs-lookup"><span data-stu-id="13db5-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="13db5-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="13db5-123">-CustomFragment</span></span>
<span data-ttu-id="13db5-124">Fragment do dodania do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="13db5-125">Fragment jest częścią adresu URL, który jest dostarczany po #.</span><span class="sxs-lookup"><span data-stu-id="13db5-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="13db5-126">Nie należy umieszczać #.</span><span class="sxs-lookup"><span data-stu-id="13db5-126">Do not include the #.</span></span>

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

### <span data-ttu-id="13db5-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="13db5-127">-CustomHostname</span></span>
<span data-ttu-id="13db5-128">Host do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-128">Host to redirect.</span></span>
<span data-ttu-id="13db5-129">Pozostaw to pole puste, aby używać hosta przychodzącego jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="13db5-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="13db5-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="13db5-130">-CustomPath</span></span>
<span data-ttu-id="13db5-131">Pełna ścieżka do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-131">The full path to redirect.</span></span>
<span data-ttu-id="13db5-132">Ścieżka nie może być pusta i musi zaczynać się od</span><span class="sxs-lookup"><span data-stu-id="13db5-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="13db5-133">Pozostaw to pole puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="13db5-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="13db5-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="13db5-134">-CustomQueryString</span></span>
<span data-ttu-id="13db5-135">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="13db5-136">Ustawienie tej wartości spowodowałoby zastąpienie dowolnego istniejącego ciągu kwerendy; Zostaw puste pole, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="13db5-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="13db5-137">Ciąg kwerendy musi być w \<key\> = \<value\> formacie.</span><span class="sxs-lookup"><span data-stu-id="13db5-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="13db5-138">?</span><span class="sxs-lookup"><span data-stu-id="13db5-138">?</span></span> <span data-ttu-id="13db5-139">Program & zostanie dodany automatycznie, więc nie należy go uwzględniać.</span><span class="sxs-lookup"><span data-stu-id="13db5-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="13db5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13db5-140">-DefaultProfile</span></span>
<span data-ttu-id="13db5-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13db5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13db5-142">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="13db5-142">-Destination</span></span>
<span data-ttu-id="13db5-143">Zdefiniuj względny adres URL, do którego będą ponownie zapisywane powyższe żądania.</span><span class="sxs-lookup"><span data-stu-id="13db5-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="13db5-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="13db5-144">-DestinationProtocol</span></span>
<span data-ttu-id="13db5-145">Protokół używany do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="13db5-146">Wartość domyślna to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="13db5-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="13db5-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="13db5-147">-HeaderActionType</span></span>
<span data-ttu-id="13db5-148">Określanie, czy nagłówek żądania lub nagłówek odpowiedzi ma być modyfikowany</span><span class="sxs-lookup"><span data-stu-id="13db5-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="13db5-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="13db5-149">-HeaderName</span></span>
<span data-ttu-id="13db5-150">Nazwa nagłówka do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="13db5-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="13db5-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="13db5-151">-PreservePath</span></span>
<span data-ttu-id="13db5-152">Czy zachować niedopasowaną ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="13db5-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="13db5-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="13db5-153">-QueryParameter</span></span>
<span data-ttu-id="13db5-154">Parametry zapytań do dołączania lub wykluczania (rozdzielany przecinkami).</span><span class="sxs-lookup"><span data-stu-id="13db5-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="13db5-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="13db5-155">-QueryStringBehavior</span></span>
<span data-ttu-id="13db5-156">Zachowanie kwerendy QueryString dla żądań</span><span class="sxs-lookup"><span data-stu-id="13db5-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="13db5-157">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="13db5-157">-RedirectType</span></span>
<span data-ttu-id="13db5-158">Typ przekierowania, którego reguła będzie używana podczas przekierowywania ruchu</span><span class="sxs-lookup"><span data-stu-id="13db5-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="13db5-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="13db5-159">-SourcePattern</span></span>
<span data-ttu-id="13db5-160">Zdefiniuj wzorzec adresu URL żądania określający typ żądań, które mogą być ponownie zapisane.</span><span class="sxs-lookup"><span data-stu-id="13db5-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="13db5-161">Jeśli wartość jest pusta, są dopasowywane wszystkie ciągi.</span><span class="sxs-lookup"><span data-stu-id="13db5-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="13db5-162">-Value</span><span class="sxs-lookup"><span data-stu-id="13db5-162">-Value</span></span>
<span data-ttu-id="13db5-163">Wartość dla określonej akcji.</span><span class="sxs-lookup"><span data-stu-id="13db5-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="13db5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13db5-164">CommonParameters</span></span>
<span data-ttu-id="13db5-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13db5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13db5-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13db5-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13db5-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13db5-167">INPUTS</span></span>

### <span data-ttu-id="13db5-168">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13db5-168">None</span></span>

## <span data-ttu-id="13db5-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13db5-169">OUTPUTS</span></span>

### <span data-ttu-id="13db5-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="13db5-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="13db5-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13db5-171">NOTES</span></span>

## <span data-ttu-id="13db5-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13db5-172">RELATED LINKS</span></span>
