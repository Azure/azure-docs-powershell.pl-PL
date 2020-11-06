---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543015"
---
# <span data-ttu-id="acb01-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="acb01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acb01-102">SYNOPSIS</span></span>
<span data-ttu-id="acb01-103">Umożliwia wyszukiwanie zasobów na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="acb01-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acb01-104">SYNTAX</span></span>

### <span data-ttu-id="acb01-105">Wyświetla listę zasobów na podstawie określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="acb01-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="acb01-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="acb01-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="acb01-107">Wyświetla listę zasobów na podstawie określonego zakresu na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="acb01-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="acb01-108">Pobieranie zasobów przy użyciu zapytania o wielu abonamentach.</span><span class="sxs-lookup"><span data-stu-id="acb01-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="acb01-109">Wyświetla listę zasobów według obiektu znacznika określonego jako HashSet.</span><span class="sxs-lookup"><span data-stu-id="acb01-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="acb01-110">Wyświetla listę zasobów według znacznika określonego jako poszczególne parametry nazwy i wartości.</span><span class="sxs-lookup"><span data-stu-id="acb01-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="acb01-111">Opis</span><span class="sxs-lookup"><span data-stu-id="acb01-111">DESCRIPTION</span></span>
<span data-ttu-id="acb01-112">Polecenie cmdlet **Find-AzureRmResource** wyszukuje zasoby na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="acb01-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="acb01-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acb01-113">EXAMPLES</span></span>

### <span data-ttu-id="acb01-114">Przykład 1. Wyszukiwanie zasobów według typu i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="acb01-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="acb01-115">To polecenie wyszukuje zasoby typu Microsoft. Web/Sites w grupach zasobów, których nazwy pasują do grupy Resources.</span><span class="sxs-lookup"><span data-stu-id="acb01-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="acb01-116">Przykład 2: Wyszukiwanie zasobów według typu i nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="acb01-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="acb01-117">To polecenie wyszukuje zasoby typu Microsoft. Web/witryny, których nazwa zasobu odpowiada testowi ciągu.</span><span class="sxs-lookup"><span data-stu-id="acb01-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="acb01-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acb01-118">PARAMETERS</span></span>

### <span data-ttu-id="acb01-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="acb01-119">-ApiVersion</span></span>
<span data-ttu-id="acb01-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="acb01-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="acb01-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="acb01-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="acb01-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="acb01-122">-ExpandProperties</span></span>
<span data-ttu-id="acb01-123">Wskazuje, że to polecenie cmdlet rozszerza właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="acb01-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="acb01-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="acb01-124">-ExtensionResourceType</span></span>
<span data-ttu-id="acb01-125">Określa typ zasobu rozszerzenia dla zasobów, dla których jest wyszukiwane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acb01-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="acb01-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="acb01-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="acb01-127">-InformationAction</span></span>
<span data-ttu-id="acb01-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="acb01-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="acb01-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="acb01-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="acb01-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="acb01-130">Continue</span></span>
- <span data-ttu-id="acb01-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="acb01-131">Ignore</span></span>
- <span data-ttu-id="acb01-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="acb01-132">Inquire</span></span>
- <span data-ttu-id="acb01-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="acb01-133">SilentlyContinue</span></span>
- <span data-ttu-id="acb01-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="acb01-134">Stop</span></span>
- <span data-ttu-id="acb01-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="acb01-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="acb01-136">-InformationVariable</span></span>
<span data-ttu-id="acb01-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="acb01-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="acb01-138">-ODataQuery</span></span>
<span data-ttu-id="acb01-139">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="acb01-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="acb01-140">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="acb01-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="acb01-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="acb01-141">-Pre</span></span>
<span data-ttu-id="acb01-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="acb01-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="acb01-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="acb01-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="acb01-144">Określa część nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="acb01-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="acb01-145">To polecenie cmdlet jest zgodne z grupami zasobów, których wartość jest podciągiem.</span><span class="sxs-lookup"><span data-stu-id="acb01-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="acb01-146">Polecenie cmdlet wyszukuje zasoby w tych grupach zasobów.</span><span class="sxs-lookup"><span data-stu-id="acb01-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="acb01-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="acb01-148">Nazwa grupy zasobów dla pełnego dopasowania.</span><span class="sxs-lookup"><span data-stu-id="acb01-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="acb01-149">-ResourceNameContains</span></span>
<span data-ttu-id="acb01-150">Określa część nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="acb01-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="acb01-151">Polecenie cmdlet wyszukuje zasoby, które zawierają tę wartość jako podciąg.</span><span class="sxs-lookup"><span data-stu-id="acb01-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="acb01-152">-ResourceNameEquals</span></span>
<span data-ttu-id="acb01-153">Nazwa zasobu dla pełnego dopasowania.</span><span class="sxs-lookup"><span data-stu-id="acb01-153">The resource name for a full match.</span></span> <span data-ttu-id="acb01-154">na przykład jeśli nazwa zasobu to testResource, możesz określić testResource.</span><span class="sxs-lookup"><span data-stu-id="acb01-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="acb01-155">-ResourceType</span></span>
<span data-ttu-id="acb01-156">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="acb01-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="acb01-157">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="acb01-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="acb01-158">To polecenie cmdlet wyszukuje zasoby określonego typu.</span><span class="sxs-lookup"><span data-stu-id="acb01-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="acb01-159">-Tag</span></span>
<span data-ttu-id="acb01-160">Filtr znacznika dla zapytania OData.</span><span class="sxs-lookup"><span data-stu-id="acb01-160">The tag filter for the OData query.</span></span> <span data-ttu-id="acb01-161">Oczekiwany format to @ {tagName = $null} lub @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="acb01-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="acb01-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="acb01-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="acb01-164">-TenantLevel</span></span>
<span data-ttu-id="acb01-165">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="acb01-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-166">-Początek</span><span class="sxs-lookup"><span data-stu-id="acb01-166">-Top</span></span>
<span data-ttu-id="acb01-167">Określa liczbę zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="acb01-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb01-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb01-168">-DefaultProfile</span></span>
<span data-ttu-id="acb01-169">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="acb01-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb01-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb01-170">CommonParameters</span></span>
<span data-ttu-id="acb01-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb01-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb01-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb01-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb01-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acb01-173">INPUTS</span></span>

## <span data-ttu-id="acb01-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acb01-174">OUTPUTS</span></span>

### <span data-ttu-id="acb01-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="acb01-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="acb01-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acb01-176">NOTES</span></span>

## <span data-ttu-id="acb01-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acb01-177">RELATED LINKS</span></span>

[<span data-ttu-id="acb01-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="acb01-179">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="acb01-180">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="acb01-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="acb01-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="acb01-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
