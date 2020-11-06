---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542348"
---
# <span data-ttu-id="5d763-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-101">New-AzureRmResource</span></span>

## <span data-ttu-id="5d763-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d763-102">SYNOPSIS</span></span>
<span data-ttu-id="5d763-103">Tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="5d763-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d763-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d763-104">SYNTAX</span></span>

### <span data-ttu-id="5d763-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d763-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d763-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5d763-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d763-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5d763-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d763-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d763-108">DESCRIPTION</span></span>
<span data-ttu-id="5d763-109">Polecenie cmdlet **New-AzureRmResource** umożliwia utworzenie zasobu platformy Azure, takiego jak witryna sieci Web, serwer bazy danych SQL Azure lub baza danych SQL Azure, w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d763-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="5d763-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d763-110">EXAMPLES</span></span>

### <span data-ttu-id="5d763-111">Przykład 1. Tworzenie zasobu</span><span class="sxs-lookup"><span data-stu-id="5d763-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="5d763-112">To polecenie tworzy zasób będący witryną sieci Web w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5d763-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="5d763-113">Przykład 2: Tworzenie zasobu przy użyciu splatting</span><span class="sxs-lookup"><span data-stu-id="5d763-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="5d763-114">To polecenie tworzy zasób będący witryną sieci Web w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5d763-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="5d763-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d763-115">PARAMETERS</span></span>

### <span data-ttu-id="5d763-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5d763-116">-ApiVersion</span></span>
<span data-ttu-id="5d763-117">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="5d763-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="5d763-118">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="5d763-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5d763-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d763-119">-AsJob</span></span>
<span data-ttu-id="5d763-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5d763-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d763-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d763-121">-DefaultProfile</span></span>
<span data-ttu-id="5d763-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d763-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d763-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5d763-123">-ExtensionResourceName</span></span>
<span data-ttu-id="5d763-124">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="5d763-125">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="5d763-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="5d763-126">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="5d763-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5d763-127">-ExtensionResourceType</span></span>
<span data-ttu-id="5d763-128">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d763-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5d763-129">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujący typ:</span><span class="sxs-lookup"><span data-stu-id="5d763-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5d763-130">-Force</span></span>
<span data-ttu-id="5d763-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5d763-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d763-132">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="5d763-132">-IsFullObject</span></span>
<span data-ttu-id="5d763-133">Wskazuje, że obiekt, który określa parametr *Właściwości* , jest pełnym obiektem.</span><span class="sxs-lookup"><span data-stu-id="5d763-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="5d763-134">-Kind</span><span class="sxs-lookup"><span data-stu-id="5d763-134">-Kind</span></span>
<span data-ttu-id="5d763-135">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-135">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="5d763-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5d763-136">-Location</span></span>
<span data-ttu-id="5d763-137">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="5d763-138">Określ lokalizację centrum danych, na przykład Centrala amerykańska lub Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="5d763-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="5d763-139">Zasób można umieścić w dowolnej lokalizacji obsługującej zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="5d763-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="5d763-140">Grupy zasobów mogą zawierać zasoby z różnych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5d763-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="5d763-141">Aby określić, które lokalizacje obsługują poszczególne typy zasobów, użyj polecenia cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="5d763-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="5d763-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5d763-142">-ODataQuery</span></span>
<span data-ttu-id="5d763-143">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="5d763-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="5d763-144">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="5d763-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5d763-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="5d763-145">-Plan</span></span>
<span data-ttu-id="5d763-146">Tabela skrótów reprezentująca właściwości planu zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d763-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d763-147">-Pre</span></span>
<span data-ttu-id="5d763-148">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="5d763-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5d763-149">-Properties</span><span class="sxs-lookup"><span data-stu-id="5d763-149">-Properties</span></span>
<span data-ttu-id="5d763-150">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="5d763-151">Ten parametr służy do określania wartości właściwości specyficznych dla typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d763-152">-ResourceGroupName</span></span>
<span data-ttu-id="5d763-153">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="5d763-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d763-154">-ResourceId</span></span>
<span data-ttu-id="5d763-155">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="5d763-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="5d763-156">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5d763-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5d763-157">-ResourceName</span></span>
<span data-ttu-id="5d763-158">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-158">Specifies the name of the resource.</span></span> <span data-ttu-id="5d763-159">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="5d763-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5d763-160">-ResourceType</span></span>
<span data-ttu-id="5d763-161">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d763-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="5d763-162">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="5d763-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d763-163">-Sku</span></span>
<span data-ttu-id="5d763-164">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="5d763-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d763-165">-Tag</span></span>
<span data-ttu-id="5d763-166">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5d763-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d763-167">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5d763-167">For example:</span></span>

<span data-ttu-id="5d763-168">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5d763-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5d763-169">-TenantLevel</span></span>
<span data-ttu-id="5d763-170">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5d763-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d763-171">-Confirm</span></span>
<span data-ttu-id="5d763-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d763-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d763-173">-WhatIf</span></span>
<span data-ttu-id="5d763-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d763-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d763-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d763-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d763-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d763-176">CommonParameters</span></span>
<span data-ttu-id="5d763-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d763-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d763-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d763-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d763-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d763-179">INPUTS</span></span>

### <span data-ttu-id="5d763-180">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5d763-180">None</span></span>
<span data-ttu-id="5d763-181">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5d763-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d763-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d763-182">OUTPUTS</span></span>

### <span data-ttu-id="5d763-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5d763-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5d763-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d763-184">NOTES</span></span>

## <span data-ttu-id="5d763-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d763-185">RELATED LINKS</span></span>

[<span data-ttu-id="5d763-186">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="5d763-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="5d763-188">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="5d763-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="5d763-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5d763-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
