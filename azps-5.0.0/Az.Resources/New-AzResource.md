---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307926"
---
# <span data-ttu-id="1c29c-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="1c29c-101">New-AzResource</span></span>

## <span data-ttu-id="1c29c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c29c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c29c-103">Tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="1c29c-103">Creates a resource.</span></span>

## <span data-ttu-id="1c29c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c29c-104">SYNTAX</span></span>

### <span data-ttu-id="1c29c-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c29c-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c29c-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="1c29c-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c29c-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="1c29c-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c29c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1c29c-108">DESCRIPTION</span></span>
<span data-ttu-id="1c29c-109">Polecenie cmdlet **New-AzResource** umożliwia utworzenie zasobu platformy Azure, takiego jak witryna sieci Web, serwer bazy danych SQL Azure lub baza danych SQL Azure, w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c29c-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="1c29c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c29c-110">EXAMPLES</span></span>

### <span data-ttu-id="1c29c-111">Przykład 1. Tworzenie zasobu</span><span class="sxs-lookup"><span data-stu-id="1c29c-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="1c29c-112">To polecenie tworzy zasób będący witryną sieci Web w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1c29c-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="1c29c-113">Przykład 2: Tworzenie zasobu przy użyciu splatting</span><span class="sxs-lookup"><span data-stu-id="1c29c-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="1c29c-114">To polecenie tworzy zasób będący witryną sieci Web w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1c29c-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="1c29c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c29c-115">PARAMETERS</span></span>

### <span data-ttu-id="1c29c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1c29c-116">-ApiVersion</span></span>
<span data-ttu-id="1c29c-117">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1c29c-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="1c29c-118">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="1c29c-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1c29c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c29c-119">-AsJob</span></span>
<span data-ttu-id="1c29c-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1c29c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c29c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c29c-121">-DefaultProfile</span></span>
<span data-ttu-id="1c29c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c29c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c29c-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="1c29c-123">-ExtensionResourceName</span></span>
<span data-ttu-id="1c29c-124">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="1c29c-125">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="1c29c-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="1c29c-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="1c29c-126">-ExtensionResourceType</span></span>
<span data-ttu-id="1c29c-127">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1c29c-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="1c29c-128">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujący typ: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="1c29c-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="1c29c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="1c29c-129">-Force</span></span>
<span data-ttu-id="1c29c-130">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1c29c-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c29c-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="1c29c-131">-IsFullObject</span></span>
<span data-ttu-id="1c29c-132">Wskazuje, że obiekt, który określa parametr *Właściwości* , jest pełnym obiektem.</span><span class="sxs-lookup"><span data-stu-id="1c29c-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="1c29c-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="1c29c-133">-Kind</span></span>
<span data-ttu-id="1c29c-134">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="1c29c-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1c29c-135">-Location</span></span>
<span data-ttu-id="1c29c-136">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="1c29c-137">Określ lokalizację centrum danych, na przykład Centrala amerykańska lub Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="1c29c-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="1c29c-138">Zasób można umieścić w dowolnej lokalizacji obsługującej zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="1c29c-139">Grupy zasobów mogą zawierać zasoby z różnych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1c29c-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="1c29c-140">Aby określić, które lokalizacje obsługują poszczególne typy zasobów, użyj polecenia cmdlet Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="1c29c-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="1c29c-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1c29c-141">-ODataQuery</span></span>
<span data-ttu-id="1c29c-142">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="1c29c-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="1c29c-143">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="1c29c-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="1c29c-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="1c29c-144">-Plan</span></span>
<span data-ttu-id="1c29c-145">Tabela skrótów reprezentująca właściwości planu zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c29c-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="1c29c-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="1c29c-146">-Pre</span></span>
<span data-ttu-id="1c29c-147">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="1c29c-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1c29c-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="1c29c-148">-Properties</span></span>
<span data-ttu-id="1c29c-149">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="1c29c-150">Ten parametr służy do określania wartości właściwości specyficznych dla typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="1c29c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c29c-151">-ResourceGroupName</span></span>
<span data-ttu-id="1c29c-152">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="1c29c-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="1c29c-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c29c-153">-ResourceId</span></span>
<span data-ttu-id="1c29c-154">Określa w pełni kwalifikowany identyfikator zasobu, łącznie z subskrypcją, jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1c29c-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="1c29c-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1c29c-155">-ResourceName</span></span>
<span data-ttu-id="1c29c-156">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-156">Specifies the name of the resource.</span></span> <span data-ttu-id="1c29c-157">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1c29c-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="1c29c-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1c29c-158">-ResourceType</span></span>
<span data-ttu-id="1c29c-159">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c29c-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="1c29c-160">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="1c29c-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="1c29c-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="1c29c-161">-Sku</span></span>
<span data-ttu-id="1c29c-162">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="1c29c-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="1c29c-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c29c-163">-Tag</span></span>
<span data-ttu-id="1c29c-164">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1c29c-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c29c-165">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1c29c-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1c29c-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1c29c-166">-TenantLevel</span></span>
<span data-ttu-id="1c29c-167">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1c29c-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="1c29c-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c29c-168">-Confirm</span></span>
<span data-ttu-id="1c29c-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c29c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c29c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c29c-170">-WhatIf</span></span>
<span data-ttu-id="1c29c-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c29c-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c29c-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c29c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c29c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c29c-173">CommonParameters</span></span>
<span data-ttu-id="1c29c-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c29c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c29c-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c29c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c29c-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c29c-176">INPUTS</span></span>

### <span data-ttu-id="1c29c-177">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c29c-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1c29c-178">System. String</span><span class="sxs-lookup"><span data-stu-id="1c29c-178">System.String</span></span>

## <span data-ttu-id="1c29c-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c29c-179">OUTPUTS</span></span>

### <span data-ttu-id="1c29c-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1c29c-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1c29c-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c29c-181">NOTES</span></span>

## <span data-ttu-id="1c29c-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c29c-182">RELATED LINKS</span></span>

[<span data-ttu-id="1c29c-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1c29c-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="1c29c-184">Przenieś — AzResource</span><span class="sxs-lookup"><span data-stu-id="1c29c-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="1c29c-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="1c29c-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="1c29c-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="1c29c-186">Set-AzResource</span></span>](./Set-AzResource.md)
