---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176371"
---
# <span data-ttu-id="7f021-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f021-101">Set-AzResource</span></span>

## <span data-ttu-id="7f021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f021-102">SYNOPSIS</span></span>
<span data-ttu-id="7f021-103">Modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="7f021-103">Modifies a resource.</span></span>

## <span data-ttu-id="7f021-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f021-104">SYNTAX</span></span>

### <span data-ttu-id="7f021-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="7f021-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f021-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f021-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f021-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7f021-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f021-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7f021-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f021-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f021-109">DESCRIPTION</span></span>
<span data-ttu-id="7f021-110">Polecenie cmdlet **Set-AzResource** modyfikuje istniejący zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f021-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="7f021-111">Określ zasób, który ma być modyfikowany według nazwy i typu lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="7f021-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="7f021-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f021-112">EXAMPLES</span></span>

### <span data-ttu-id="7f021-113">Przykład 1. Modyfikowanie zasobu</span><span class="sxs-lookup"><span data-stu-id="7f021-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="7f021-114">Pierwsze polecenie pobiera zasób o nazwie ContosoSite za pomocą polecenia cmdlet Get-AzResource, a następnie zapisuje go w $Resource zmienną.</span><span class="sxs-lookup"><span data-stu-id="7f021-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="7f021-115">Drugie polecenie modyfikuje właściwość $Resource.</span><span class="sxs-lookup"><span data-stu-id="7f021-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="7f021-116">Ostatnie polecenie aktualizuje zasób w celu dopasowania go $Resource.</span><span class="sxs-lookup"><span data-stu-id="7f021-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="7f021-117">Przykład 2. Modyfikowanie wszystkich zasobów w danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="7f021-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="7f021-118">Pierwsze polecenie pobiera zasoby do grupy zasobów testrg, a następnie przechowuje je w $Resource zmienną.</span><span class="sxs-lookup"><span data-stu-id="7f021-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="7f021-119">Drugie polecenie będzie korzystać z iterowania każdego z tych zasobów w grupie zasobów i dodaje do nich nowy tag.</span><span class="sxs-lookup"><span data-stu-id="7f021-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="7f021-120">Ostatnie polecenie aktualizuje każdy z tych zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f021-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="7f021-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f021-121">PARAMETERS</span></span>

### <span data-ttu-id="7f021-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f021-122">-ApiVersion</span></span>
<span data-ttu-id="7f021-123">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="7f021-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7f021-124">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="7f021-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7f021-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7f021-125">-AsJob</span></span>
<span data-ttu-id="7f021-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7f021-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f021-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f021-127">-DefaultProfile</span></span>
<span data-ttu-id="7f021-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7f021-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f021-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7f021-129">-ExtensionResourceName</span></span>
<span data-ttu-id="7f021-130">Określa nazwę zasobu rozszerzenia dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="7f021-131">Aby na przykład określić bazę danych, należy użyć następującego formatu: nazwa bazy danych o `/` nazwie serwera.</span><span class="sxs-lookup"><span data-stu-id="7f021-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="7f021-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7f021-132">-ExtensionResourceType</span></span>
<span data-ttu-id="7f021-133">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="7f021-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="7f021-134">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujące informacje: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="7f021-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="7f021-135">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7f021-135">-Force</span></span>
<span data-ttu-id="7f021-136">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7f021-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f021-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f021-137">-InputObject</span></span>
<span data-ttu-id="7f021-138">Obiektowa reprezentacja zasobu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7f021-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f021-139">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="7f021-139">-Kind</span></span>
<span data-ttu-id="7f021-140">Określa rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f021-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7f021-141">-ODataQuery</span></span>
<span data-ttu-id="7f021-142">Określa filtr stylu protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="7f021-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7f021-143">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="7f021-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7f021-144">— planowanie</span><span class="sxs-lookup"><span data-stu-id="7f021-144">-Plan</span></span>
<span data-ttu-id="7f021-145">Określa właściwości planu zasobów jako tabelę skrótów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f021-146">— Przed</span><span class="sxs-lookup"><span data-stu-id="7f021-146">-Pre</span></span>
<span data-ttu-id="7f021-147">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="7f021-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7f021-148">— Properties</span><span class="sxs-lookup"><span data-stu-id="7f021-148">-Properties</span></span>
<span data-ttu-id="7f021-149">Określa właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f021-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f021-150">-ResourceGroupName</span></span>
<span data-ttu-id="7f021-151">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="7f021-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="7f021-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f021-152">-ResourceId</span></span>
<span data-ttu-id="7f021-153">Określa w pełni kwalifikowany identyfikator zasobu, łącznie z subskrypcją, jak w poniższym `/subscriptions/` przykładzie: Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7f021-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="7f021-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7f021-154">-ResourceName</span></span>
<span data-ttu-id="7f021-155">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="7f021-156">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7f021-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="7f021-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7f021-157">-ResourceType</span></span>
<span data-ttu-id="7f021-158">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f021-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="7f021-159">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="7f021-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="7f021-160">- SKU</span><span class="sxs-lookup"><span data-stu-id="7f021-160">-Sku</span></span>
<span data-ttu-id="7f021-161">Określa obiekt SKU zasobu jako tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="7f021-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="7f021-162">— Tag</span><span class="sxs-lookup"><span data-stu-id="7f021-162">-Tag</span></span>
<span data-ttu-id="7f021-163">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="7f021-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f021-164">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7f021-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f021-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7f021-165">-TenantLevel</span></span>
<span data-ttu-id="7f021-166">Wskazuje, że to polecenie cmdlet działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7f021-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="7f021-167">—UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="7f021-167">-UsePatchSemantics</span></span>
<span data-ttu-id="7f021-168">Wskazuje, że to polecenie cmdlet używa poprawki HTTP w celu zaktualizowania obiektu zamiast protokołu HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="7f021-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="7f021-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f021-169">-Confirm</span></span>
<span data-ttu-id="7f021-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f021-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f021-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f021-171">-WhatIf</span></span>
<span data-ttu-id="7f021-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f021-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f021-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f021-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f021-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f021-174">CommonParameters</span></span>
<span data-ttu-id="7f021-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f021-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f021-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f021-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f021-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f021-177">INPUTS</span></span>

### <span data-ttu-id="7f021-178">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="7f021-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="7f021-179">System.String</span><span class="sxs-lookup"><span data-stu-id="7f021-179">System.String</span></span>

### <span data-ttu-id="7f021-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7f021-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="7f021-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f021-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f021-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f021-182">OUTPUTS</span></span>

### <span data-ttu-id="7f021-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7f021-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7f021-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f021-184">NOTES</span></span>

## <span data-ttu-id="7f021-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f021-185">RELATED LINKS</span></span>

[<span data-ttu-id="7f021-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f021-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="7f021-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f021-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="7f021-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f021-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="7f021-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f021-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
