---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: eea8d72285e478f9eecb0a34f80cae5787ecec83
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405299"
---
# <span data-ttu-id="d72a4-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="d72a4-101">New-AzResource</span></span>

## <span data-ttu-id="d72a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d72a4-103">Tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="d72a4-103">Creates a resource.</span></span>

## <span data-ttu-id="d72a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d72a4-104">SYNTAX</span></span>

### <span data-ttu-id="d72a4-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="d72a4-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d72a4-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d72a4-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72a4-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d72a4-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d72a4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d72a4-108">DESCRIPTION</span></span>
<span data-ttu-id="d72a4-109">Polecenie **cmdlet New-AzResource** tworzy zasób azure, taki jak witryna internetowa, serwer Azure SQL Database lub baza danych Azure SQL Database, w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d72a4-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="d72a4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d72a4-110">EXAMPLES</span></span>

### <span data-ttu-id="d72a4-111">Przykład 1. Tworzenie zasobu</span><span class="sxs-lookup"><span data-stu-id="d72a4-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="d72a4-112">To polecenie tworzy zasób, który jest witryną sieci Web w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="d72a4-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="d72a4-113">Przykład 2. Tworzenie zasobu przy użyciu usługi Splatting</span><span class="sxs-lookup"><span data-stu-id="d72a4-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="d72a4-114">To polecenie tworzy zasób, który jest witryną sieci Web w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="d72a4-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="d72a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72a4-115">PARAMETERS</span></span>

### <span data-ttu-id="d72a4-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d72a4-116">-ApiVersion</span></span>
<span data-ttu-id="d72a4-117">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="d72a4-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="d72a4-118">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d72a4-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d72a4-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d72a4-119">-AsJob</span></span>
<span data-ttu-id="d72a4-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d72a4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d72a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72a4-121">-DefaultProfile</span></span>
<span data-ttu-id="d72a4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d72a4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72a4-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d72a4-123">-ExtensionResourceName</span></span>
<span data-ttu-id="d72a4-124">Określa nazwę zasobu rozszerzenia dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="d72a4-125">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa bazy danych o `/` nazwie serwera</span><span class="sxs-lookup"><span data-stu-id="d72a4-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d72a4-126">-ExtensionResourceType</span></span>
<span data-ttu-id="d72a4-127">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d72a4-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="d72a4-128">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujący typ: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="d72a4-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d72a4-129">-Force</span></span>
<span data-ttu-id="d72a4-130">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d72a4-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d72a4-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="d72a4-131">-IsFullObject</span></span>
<span data-ttu-id="d72a4-132">Wskazuje, że obiekt, który parametr *Properties* określa, jest pełnym obiektem.</span><span class="sxs-lookup"><span data-stu-id="d72a4-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="d72a4-133">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="d72a4-133">-Kind</span></span>
<span data-ttu-id="d72a4-134">Określa rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="d72a4-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d72a4-135">-Location</span></span>
<span data-ttu-id="d72a4-136">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="d72a4-137">Określ lokalizację centrum danych, na przykład Środkowe Stanów Zjednoczonych lub Azji Południowo-Wschodniej.</span><span class="sxs-lookup"><span data-stu-id="d72a4-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="d72a4-138">Zasób można umieścić w dowolnej lokalizacji obsługującej zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="d72a4-139">Grupy zasobów mogą zawierać zasoby z różnych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d72a4-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="d72a4-140">Aby określić lokalizacje, które obsługują poszczególne typy zasobów, użyj Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72a4-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="d72a4-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d72a4-141">-ODataQuery</span></span>
<span data-ttu-id="d72a4-142">Określa filtr stylu protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="d72a4-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="d72a4-143">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="d72a4-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="d72a4-144">— planowanie</span><span class="sxs-lookup"><span data-stu-id="d72a4-144">-Plan</span></span>
<span data-ttu-id="d72a4-145">Tabela skrótów reprezentująca właściwości planu zasobów.</span><span class="sxs-lookup"><span data-stu-id="d72a4-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-146">— Przed</span><span class="sxs-lookup"><span data-stu-id="d72a4-146">-Pre</span></span>
<span data-ttu-id="d72a4-147">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d72a4-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d72a4-148">— Properties</span><span class="sxs-lookup"><span data-stu-id="d72a4-148">-Properties</span></span>
<span data-ttu-id="d72a4-149">Określa właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="d72a4-150">Ten parametr służy do określania wartości właściwości specyficznych dla typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72a4-151">-ResourceGroupName</span></span>
<span data-ttu-id="d72a4-152">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="d72a4-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d72a4-153">-ResourceId</span></span>
<span data-ttu-id="d72a4-154">Określa w pełni kwalifikowany identyfikator zasobu, łącznie z subskrypcją, jak w poniższym `/subscriptions/` przykładzie: Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d72a4-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d72a4-155">-ResourceName</span></span>
<span data-ttu-id="d72a4-156">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-156">Specifies the name of the resource.</span></span> <span data-ttu-id="d72a4-157">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d72a4-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d72a4-158">-ResourceType</span></span>
<span data-ttu-id="d72a4-159">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="d72a4-160">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="d72a4-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-161">- SKU</span><span class="sxs-lookup"><span data-stu-id="d72a4-161">-Sku</span></span>
<span data-ttu-id="d72a4-162">Tabela skrótów reprezentująca właściwości sKU.</span><span class="sxs-lookup"><span data-stu-id="d72a4-162">A hash table that represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-163">— Tag</span><span class="sxs-lookup"><span data-stu-id="d72a4-163">-Tag</span></span>
<span data-ttu-id="d72a4-164">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="d72a4-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d72a4-165">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d72a4-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d72a4-166">-TenantLevel</span></span>
<span data-ttu-id="d72a4-167">Wskazuje, że to polecenie cmdlet działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d72a4-167">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d72a4-168">-Confirm</span></span>
<span data-ttu-id="d72a4-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d72a4-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72a4-170">-WhatIf</span></span>
<span data-ttu-id="d72a4-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72a4-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72a4-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d72a4-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72a4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72a4-173">CommonParameters</span></span>
<span data-ttu-id="d72a4-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72a4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72a4-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d72a4-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72a4-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72a4-176">INPUTS</span></span>

### <span data-ttu-id="d72a4-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d72a4-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d72a4-178">System.String</span><span class="sxs-lookup"><span data-stu-id="d72a4-178">System.String</span></span>

## <span data-ttu-id="d72a4-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72a4-179">OUTPUTS</span></span>

### <span data-ttu-id="d72a4-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="d72a4-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d72a4-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d72a4-181">NOTES</span></span>

## <span data-ttu-id="d72a4-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d72a4-182">RELATED LINKS</span></span>


[<span data-ttu-id="d72a4-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d72a4-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="d72a4-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="d72a4-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="d72a4-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="d72a4-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="d72a4-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="d72a4-186">Set-AzResource</span></span>](./Set-AzResource.md)
