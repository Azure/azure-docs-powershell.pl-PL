---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550792"
---
# <span data-ttu-id="18318-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-101">New-AzureRmResource</span></span>

## <span data-ttu-id="18318-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18318-102">SYNOPSIS</span></span>
<span data-ttu-id="18318-103">Tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="18318-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18318-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18318-104">SYNTAX</span></span>

### <span data-ttu-id="18318-105">Identyfikator zasobu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="18318-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18318-106">Zasób znajdujący się na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="18318-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18318-107">Zasób znajdujący się na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="18318-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18318-108">Opis</span><span class="sxs-lookup"><span data-stu-id="18318-108">DESCRIPTION</span></span>
<span data-ttu-id="18318-109">Polecenie cmdlet **New-AzureRmResource** umożliwia utworzenie zasobu platformy Azure, takiego jak witryna sieci Web, serwer bazy danych SQL Azure lub baza danych SQL Azure, w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="18318-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="18318-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18318-110">EXAMPLES</span></span>

### <span data-ttu-id="18318-111">Przykład 1. Tworzenie zasobu</span><span class="sxs-lookup"><span data-stu-id="18318-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="18318-112">To polecenie tworzy zasób będący witryną sieci Web w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="18318-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="18318-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18318-113">PARAMETERS</span></span>

### <span data-ttu-id="18318-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18318-114">-ApiVersion</span></span>
<span data-ttu-id="18318-115">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="18318-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="18318-116">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="18318-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="18318-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="18318-117">-ExtensionResourceName</span></span>
<span data-ttu-id="18318-118">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="18318-119">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="18318-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="18318-120">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="18318-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="18318-121">-ExtensionResourceType</span></span>
<span data-ttu-id="18318-122">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="18318-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="18318-123">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujący typ:</span><span class="sxs-lookup"><span data-stu-id="18318-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-124">-Force</span><span class="sxs-lookup"><span data-stu-id="18318-124">-Force</span></span>
<span data-ttu-id="18318-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18318-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18318-126">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="18318-126">-IsFullObject</span></span>
<span data-ttu-id="18318-127">Wskazuje, że obiekt, który określa parametr *Właściwości* , jest pełnym obiektem.</span><span class="sxs-lookup"><span data-stu-id="18318-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="18318-128">-Kind</span><span class="sxs-lookup"><span data-stu-id="18318-128">-Kind</span></span>
<span data-ttu-id="18318-129">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="18318-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18318-130">-Location</span></span>
<span data-ttu-id="18318-131">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="18318-132">Określ lokalizację centrum danych, na przykład Centrala amerykańska lub Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="18318-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="18318-133">Zasób można umieścić w dowolnej lokalizacji obsługującej zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="18318-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="18318-134">Grupy zasobów mogą zawierać zasoby z różnych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="18318-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="18318-135">Aby określić, które lokalizacje obsługują poszczególne typy zasobów, użyj polecenia cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="18318-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="18318-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="18318-136">-ODataQuery</span></span>
<span data-ttu-id="18318-137">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="18318-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="18318-138">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="18318-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="18318-139">-Plan</span><span class="sxs-lookup"><span data-stu-id="18318-139">-Plan</span></span>
<span data-ttu-id="18318-140">Tabela skrótów reprezentująca właściwości planu zasobów.</span><span class="sxs-lookup"><span data-stu-id="18318-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="18318-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="18318-141">-Pre</span></span>
<span data-ttu-id="18318-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="18318-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="18318-143">-Properties</span><span class="sxs-lookup"><span data-stu-id="18318-143">-Properties</span></span>
<span data-ttu-id="18318-144">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="18318-145">Ten parametr służy do określania wartości właściwości specyficznych dla typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="18318-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18318-146">-ResourceGroupName</span></span>
<span data-ttu-id="18318-147">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy zasób.</span><span class="sxs-lookup"><span data-stu-id="18318-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18318-148">-ResourceId</span></span>
<span data-ttu-id="18318-149">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="18318-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="18318-150">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="18318-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="18318-151">-ResourceName</span></span>
<span data-ttu-id="18318-152">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-152">Specifies the name of the resource.</span></span> <span data-ttu-id="18318-153">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="18318-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="18318-154">-ResourceType</span></span>
<span data-ttu-id="18318-155">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="18318-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="18318-156">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="18318-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18318-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="18318-157">-Sku</span></span>
<span data-ttu-id="18318-158">Tabela skrótów reprezentująca właściwości jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="18318-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="18318-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="18318-159">-Tag</span></span>
<span data-ttu-id="18318-160">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="18318-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18318-161">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="18318-161">For example:</span></span>

<span data-ttu-id="18318-162">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="18318-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="18318-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="18318-163">-TenantLevel</span></span>
<span data-ttu-id="18318-164">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="18318-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18318-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18318-165">-Confirm</span></span>
<span data-ttu-id="18318-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18318-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18318-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18318-167">-WhatIf</span></span>
<span data-ttu-id="18318-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18318-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18318-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18318-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18318-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18318-170">-DefaultProfile</span></span>
<span data-ttu-id="18318-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18318-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18318-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18318-172">CommonParameters</span></span>
<span data-ttu-id="18318-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18318-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18318-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18318-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18318-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18318-175">INPUTS</span></span>

## <span data-ttu-id="18318-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18318-176">OUTPUTS</span></span>

### <span data-ttu-id="18318-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="18318-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="18318-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18318-178">NOTES</span></span>

## <span data-ttu-id="18318-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18318-179">RELATED LINKS</span></span>

[<span data-ttu-id="18318-180">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="18318-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="18318-182">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="18318-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="18318-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="18318-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
