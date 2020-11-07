---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706553"
---
# <span data-ttu-id="1c69f-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="1c69f-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="1c69f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c69f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c69f-103">Umożliwia utworzenie akcji dostarczania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-103">Creates a delivery action.</span></span>

## <span data-ttu-id="1c69f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c69f-104">SYNTAX</span></span>

### <span data-ttu-id="1c69f-105">CacheExpirationActionParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c69f-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c69f-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c69f-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c69f-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c69f-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c69f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1c69f-108">DESCRIPTION</span></span>
<span data-ttu-id="1c69f-109">Polecenie cmdlet **New-AzCdnDeliveryRule** umożliwia utworzenie reguły dostarczania dla tworzenia punktu końcowego usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="1c69f-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="1c69f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c69f-110">EXAMPLES</span></span>

### <span data-ttu-id="1c69f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c69f-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="1c69f-112">Tworzenie prostej reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="1c69f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c69f-113">PARAMETERS</span></span>

### <span data-ttu-id="1c69f-114">-Action</span><span class="sxs-lookup"><span data-stu-id="1c69f-114">-Action</span></span>
<span data-ttu-id="1c69f-115">Akcja do wykonania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-115">Action to perform.</span></span>

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

### <span data-ttu-id="1c69f-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="1c69f-116">-CacheBehavior</span></span>
<span data-ttu-id="1c69f-117">Zachowanie funkcji buforowania dla akcji</span><span class="sxs-lookup"><span data-stu-id="1c69f-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="1c69f-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="1c69f-118">-CacheDuration</span></span>
<span data-ttu-id="1c69f-119">Czas trwania, dla którego zawartość musi być buforowana.</span><span class="sxs-lookup"><span data-stu-id="1c69f-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="1c69f-120">Dozwolony format to \[ d. \] GG: mm: SS</span><span class="sxs-lookup"><span data-stu-id="1c69f-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="1c69f-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="1c69f-121">-CustomFragment</span></span>
<span data-ttu-id="1c69f-122">Fragment do dodania do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="1c69f-123">Fragment jest częścią adresu URL, który jest dostarczany po #.</span><span class="sxs-lookup"><span data-stu-id="1c69f-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="1c69f-124">Nie należy umieszczać #.</span><span class="sxs-lookup"><span data-stu-id="1c69f-124">Do not include the #.</span></span>

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

### <span data-ttu-id="1c69f-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="1c69f-125">-CustomHostname</span></span>
<span data-ttu-id="1c69f-126">Host do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-126">Host to redirect.</span></span>
<span data-ttu-id="1c69f-127">Pozostaw to pole puste, aby używać hosta przychodzącego jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="1c69f-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="1c69f-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="1c69f-128">-CustomPath</span></span>
<span data-ttu-id="1c69f-129">Pełna ścieżka do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-129">The full path to redirect.</span></span>
<span data-ttu-id="1c69f-130">Ścieżka nie może być pusta i musi zaczynać się od</span><span class="sxs-lookup"><span data-stu-id="1c69f-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="1c69f-131">Pozostaw to pole puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="1c69f-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="1c69f-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="1c69f-132">-CustomQueryString</span></span>
<span data-ttu-id="1c69f-133">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="1c69f-134">Ustawienie tej wartości spowodowałoby zastąpienie dowolnego istniejącego ciągu kwerendy; Zostaw puste pole, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="1c69f-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="1c69f-135">Ciąg kwerendy musi mieć \< \> = \< format wartości klucza \> .</span><span class="sxs-lookup"><span data-stu-id="1c69f-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="1c69f-136">?</span><span class="sxs-lookup"><span data-stu-id="1c69f-136">?</span></span> <span data-ttu-id="1c69f-137">Program & zostanie dodany automatycznie, więc nie należy go uwzględniać.</span><span class="sxs-lookup"><span data-stu-id="1c69f-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="1c69f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c69f-138">-DefaultProfile</span></span>
<span data-ttu-id="1c69f-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c69f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c69f-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="1c69f-140">-DestinationProtocol</span></span>
<span data-ttu-id="1c69f-141">Protokół używany do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="1c69f-142">Wartość domyślna to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="1c69f-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="1c69f-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="1c69f-143">-HeaderActionType</span></span>
<span data-ttu-id="1c69f-144">Określanie, czy nagłówek żądania lub nagłówek odpowiedzi ma być modyfikowany</span><span class="sxs-lookup"><span data-stu-id="1c69f-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="1c69f-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="1c69f-145">-HeaderName</span></span>
<span data-ttu-id="1c69f-146">Nazwa nagłówka do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="1c69f-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="1c69f-147">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="1c69f-147">-RedirectType</span></span>
<span data-ttu-id="1c69f-148">Typ przekierowania, którego reguła będzie używana podczas przekierowywania ruchu</span><span class="sxs-lookup"><span data-stu-id="1c69f-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="1c69f-149">-Value</span><span class="sxs-lookup"><span data-stu-id="1c69f-149">-Value</span></span>
<span data-ttu-id="1c69f-150">Wartość dla określonej akcji.</span><span class="sxs-lookup"><span data-stu-id="1c69f-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="1c69f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c69f-151">CommonParameters</span></span>
<span data-ttu-id="1c69f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c69f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c69f-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c69f-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c69f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c69f-154">INPUTS</span></span>

### <span data-ttu-id="1c69f-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1c69f-155">None</span></span>

## <span data-ttu-id="1c69f-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c69f-156">OUTPUTS</span></span>

### <span data-ttu-id="1c69f-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="1c69f-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="1c69f-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c69f-158">NOTES</span></span>

## <span data-ttu-id="1c69f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c69f-159">RELATED LINKS</span></span>
