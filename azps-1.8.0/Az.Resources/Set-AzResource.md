---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: a47d9a985adba97659ffac84d054b418daf1bc02
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "93719700"
---
# <span data-ttu-id="a12e9-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-101">Set-AzResource</span></span>

## <span data-ttu-id="a12e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a12e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a12e9-103">Modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="a12e9-103">Modifies a resource.</span></span>

## <span data-ttu-id="a12e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a12e9-104">SYNTAX</span></span>

### <span data-ttu-id="a12e9-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a12e9-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a12e9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a12e9-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a12e9-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a12e9-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e9-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a12e9-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a12e9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a12e9-109">DESCRIPTION</span></span>
<span data-ttu-id="a12e9-110">Polecenie cmdlet **Set-AzResource** modyfikuje istniejący zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a12e9-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="a12e9-111">Określ zasób do zmodyfikowania według nazwy i typu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a12e9-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="a12e9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a12e9-112">EXAMPLES</span></span>

### <span data-ttu-id="a12e9-113">Przykład 1. Modyfikowanie zasobu</span><span class="sxs-lookup"><span data-stu-id="a12e9-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="a12e9-114">Pierwsze polecenie uzyskuje zasób o nazwie ContosoSite przy użyciu polecenia cmdlet Get-AzResource, a następnie zapisuje go w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="a12e9-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="a12e9-115">Drugie polecenie modyfikuje Właściwość $Resource.</span><span class="sxs-lookup"><span data-stu-id="a12e9-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="a12e9-116">Polecenie ostatnie powoduje zaktualizowanie zasobu w celu dopasowania $Resource.</span><span class="sxs-lookup"><span data-stu-id="a12e9-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="a12e9-117">Przykład 2: modyfikowanie wszystkich zasobów w danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a12e9-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="a12e9-118">Pierwsze polecenie uzyskuje zasoby w grupie zasobów testrg, a następnie zapisuje je w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="a12e9-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="a12e9-119">Drugie polecenie powtórzy wszystkie te zasoby w grupie zasobów i doda do nich nowy znacznik.</span><span class="sxs-lookup"><span data-stu-id="a12e9-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="a12e9-120">Polecenie ostatnie umożliwia zaktualizowanie każdego z tych zasobów.</span><span class="sxs-lookup"><span data-stu-id="a12e9-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="a12e9-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a12e9-121">PARAMETERS</span></span>

### <span data-ttu-id="a12e9-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a12e9-122">-ApiVersion</span></span>
<span data-ttu-id="a12e9-123">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="a12e9-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a12e9-124">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="a12e9-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a12e9-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a12e9-125">-AsJob</span></span>
<span data-ttu-id="a12e9-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a12e9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a12e9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12e9-127">-DefaultProfile</span></span>
<span data-ttu-id="a12e9-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a12e9-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a12e9-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a12e9-129">-ExtensionResourceName</span></span>
<span data-ttu-id="a12e9-130">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="a12e9-131">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="a12e9-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a12e9-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a12e9-132">-ExtensionResourceType</span></span>
<span data-ttu-id="a12e9-133">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a12e9-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a12e9-134">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujące elementy: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a12e9-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a12e9-135">-Force</span><span class="sxs-lookup"><span data-stu-id="a12e9-135">-Force</span></span>
<span data-ttu-id="a12e9-136">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a12e9-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a12e9-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a12e9-137">-InputObject</span></span>
<span data-ttu-id="a12e9-138">Reprezentacja obiektu zasobu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="a12e9-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="a12e9-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="a12e9-139">-Kind</span></span>
<span data-ttu-id="a12e9-140">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a12e9-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a12e9-141">-ODataQuery</span></span>
<span data-ttu-id="a12e9-142">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a12e9-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="a12e9-143">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="a12e9-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a12e9-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="a12e9-144">-Plan</span></span>
<span data-ttu-id="a12e9-145">Określa właściwości planu zasobów jako tabelę skrótów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="a12e9-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="a12e9-146">-Pre</span></span>
<span data-ttu-id="a12e9-147">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="a12e9-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a12e9-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="a12e9-148">-Properties</span></span>
<span data-ttu-id="a12e9-149">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="a12e9-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12e9-150">-ResourceGroupName</span></span>
<span data-ttu-id="a12e9-151">Określa nazwę grupy zasobów, w której to polecenie cmdlet modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="a12e9-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="a12e9-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a12e9-152">-ResourceId</span></span>
<span data-ttu-id="a12e9-153">Określa w pełni kwalifikowany identyfikator zasobu, łącznie z subskrypcją, jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a12e9-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a12e9-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a12e9-154">-ResourceName</span></span>
<span data-ttu-id="a12e9-155">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="a12e9-156">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a12e9-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a12e9-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a12e9-157">-ResourceType</span></span>
<span data-ttu-id="a12e9-158">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e9-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="a12e9-159">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a12e9-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a12e9-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="a12e9-160">-Sku</span></span>
<span data-ttu-id="a12e9-161">Określa obiekt SKU zasobu jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a12e9-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="a12e9-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="a12e9-162">-Tag</span></span>
<span data-ttu-id="a12e9-163">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a12e9-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a12e9-164">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a12e9-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a12e9-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a12e9-165">-TenantLevel</span></span>
<span data-ttu-id="a12e9-166">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a12e9-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a12e9-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="a12e9-167">-UsePatchSemantics</span></span>
<span data-ttu-id="a12e9-168">Wskazuje, że w tym poleceniu cmdlet jest używana poprawka HTTP w celu zaktualizowania obiektu zamiast funkcji PUT HTTP.</span><span class="sxs-lookup"><span data-stu-id="a12e9-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="a12e9-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a12e9-169">-Confirm</span></span>
<span data-ttu-id="a12e9-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a12e9-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12e9-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12e9-171">-WhatIf</span></span>
<span data-ttu-id="a12e9-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a12e9-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a12e9-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a12e9-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12e9-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12e9-174">CommonParameters</span></span>
<span data-ttu-id="a12e9-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12e9-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12e9-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a12e9-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12e9-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a12e9-177">INPUTS</span></span>

### <span data-ttu-id="a12e9-178">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="a12e9-179">System. String</span><span class="sxs-lookup"><span data-stu-id="a12e9-179">System.String</span></span>

### <span data-ttu-id="a12e9-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a12e9-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="a12e9-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a12e9-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a12e9-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a12e9-182">OUTPUTS</span></span>

### <span data-ttu-id="a12e9-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a12e9-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a12e9-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a12e9-184">NOTES</span></span>

## <span data-ttu-id="a12e9-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a12e9-185">RELATED LINKS</span></span>

[<span data-ttu-id="a12e9-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="a12e9-187">Przenieś — AzResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="a12e9-188">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="a12e9-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="a12e9-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
