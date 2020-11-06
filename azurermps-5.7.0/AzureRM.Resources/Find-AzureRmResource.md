---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548027"
---
# <span data-ttu-id="9b719-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="9b719-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b719-102">SYNOPSIS</span></span>
<span data-ttu-id="9b719-103">Umożliwia wyszukiwanie zasobów na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="9b719-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b719-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b719-104">SYNTAX</span></span>

### <span data-ttu-id="9b719-105">GetBySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b719-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b719-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9b719-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b719-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="9b719-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b719-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="9b719-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b719-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="9b719-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b719-110">Opis</span><span class="sxs-lookup"><span data-stu-id="9b719-110">DESCRIPTION</span></span>
<span data-ttu-id="9b719-111">Polecenie cmdlet **Find-AzureRmResource** wyszukuje zasoby na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="9b719-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="9b719-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b719-112">EXAMPLES</span></span>

### <span data-ttu-id="9b719-113">Przykład 1. Wyszukiwanie zasobów według typu i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9b719-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="9b719-114">To polecenie wyszukuje zasoby typu Microsoft. Web/Sites w grupach zasobów, których nazwy pasują do grupy Resources.</span><span class="sxs-lookup"><span data-stu-id="9b719-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="9b719-115">Przykład 2: Wyszukiwanie zasobów według typu i nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="9b719-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="9b719-116">To polecenie wyszukuje zasoby typu Microsoft. Web/witryny, których nazwa zasobu odpowiada testowi ciągu.</span><span class="sxs-lookup"><span data-stu-id="9b719-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="9b719-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b719-117">PARAMETERS</span></span>

### <span data-ttu-id="9b719-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9b719-118">-ApiVersion</span></span>
<span data-ttu-id="9b719-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="9b719-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9b719-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="9b719-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b719-121">-DefaultProfile</span></span>
<span data-ttu-id="9b719-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9b719-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="9b719-123">-ExpandProperties</span></span>
<span data-ttu-id="9b719-124">Wskazuje, że to polecenie cmdlet rozszerza właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="9b719-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9b719-125">-ExtensionResourceType</span></span>
<span data-ttu-id="9b719-126">Określa typ zasobu rozszerzenia dla zasobów, dla których jest wyszukiwane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b719-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="9b719-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="9b719-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9b719-128">-InformationAction</span></span>
<span data-ttu-id="9b719-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9b719-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b719-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9b719-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b719-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9b719-131">Continue</span></span>
- <span data-ttu-id="9b719-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9b719-132">Ignore</span></span>
- <span data-ttu-id="9b719-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="9b719-133">Inquire</span></span>
- <span data-ttu-id="9b719-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b719-134">SilentlyContinue</span></span>
- <span data-ttu-id="9b719-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9b719-135">Stop</span></span>
- <span data-ttu-id="9b719-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9b719-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b719-137">-InformationVariable</span></span>
<span data-ttu-id="9b719-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9b719-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9b719-139">-ODataQuery</span></span>
<span data-ttu-id="9b719-140">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="9b719-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9b719-141">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="9b719-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="9b719-142">-Pre</span></span>
<span data-ttu-id="9b719-143">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="9b719-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="9b719-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="9b719-145">Określa część nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b719-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="9b719-146">To polecenie cmdlet jest zgodne z grupami zasobów, których wartość jest podciągiem.</span><span class="sxs-lookup"><span data-stu-id="9b719-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="9b719-147">Polecenie cmdlet wyszukuje zasoby w tych grupach zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b719-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="9b719-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="9b719-149">Nazwa grupy zasobów dla pełnego dopasowania.</span><span class="sxs-lookup"><span data-stu-id="9b719-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="9b719-150">-ResourceNameContains</span></span>
<span data-ttu-id="9b719-151">Określa część nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="9b719-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="9b719-152">Polecenie cmdlet wyszukuje zasoby, które zawierają tę wartość jako podciąg.</span><span class="sxs-lookup"><span data-stu-id="9b719-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="9b719-153">-ResourceNameEquals</span></span>
<span data-ttu-id="9b719-154">Nazwa zasobu dla pełnego dopasowania.</span><span class="sxs-lookup"><span data-stu-id="9b719-154">The resource name for a full match.</span></span> <span data-ttu-id="9b719-155">na przykład jeśli nazwa zasobu to testResource, możesz określić testResource.</span><span class="sxs-lookup"><span data-stu-id="9b719-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9b719-156">-ResourceType</span></span>
<span data-ttu-id="9b719-157">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="9b719-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="9b719-158">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="9b719-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="9b719-159">To polecenie cmdlet wyszukuje zasoby określonego typu.</span><span class="sxs-lookup"><span data-stu-id="9b719-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b719-160">-Tag</span></span>
<span data-ttu-id="9b719-161">Filtr znacznika dla zapytania OData.</span><span class="sxs-lookup"><span data-stu-id="9b719-161">The tag filter for the OData query.</span></span> <span data-ttu-id="9b719-162">Oczekiwany format to @ {tagName = $null} lub @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="9b719-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="9b719-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="9b719-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9b719-165">-TenantLevel</span></span>
<span data-ttu-id="9b719-166">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9b719-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-167">-Początek</span><span class="sxs-lookup"><span data-stu-id="9b719-167">-Top</span></span>
<span data-ttu-id="9b719-168">Określa liczbę zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9b719-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b719-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b719-169">CommonParameters</span></span>
<span data-ttu-id="9b719-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b719-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b719-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b719-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b719-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b719-172">INPUTS</span></span>

### <span data-ttu-id="9b719-173">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9b719-173">None</span></span>
<span data-ttu-id="9b719-174">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9b719-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b719-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b719-175">OUTPUTS</span></span>

### <span data-ttu-id="9b719-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9b719-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9b719-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b719-177">NOTES</span></span>

## <span data-ttu-id="9b719-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b719-178">RELATED LINKS</span></span>

[<span data-ttu-id="9b719-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="9b719-180">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9b719-181">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9b719-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9b719-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9b719-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
