---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718704"
---
# <span data-ttu-id="12ff5-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="12ff5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="12ff5-103">Modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="12ff5-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ff5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12ff5-104">SYNTAX</span></span>

### <span data-ttu-id="12ff5-105">Identyfikator zasobu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="12ff5-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12ff5-106">Zasób znajdujący się na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ff5-107">Zasób znajdujący się na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="12ff5-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12ff5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="12ff5-108">DESCRIPTION</span></span>
<span data-ttu-id="12ff5-109">Polecenie cmdlet **Set-AzureRmResource** modyfikuje istniejący zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12ff5-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="12ff5-110">Określ zasób do zmodyfikowania według nazwy i typu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="12ff5-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="12ff5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12ff5-111">EXAMPLES</span></span>

### <span data-ttu-id="12ff5-112">Przykład 1. Modyfikowanie zasobu</span><span class="sxs-lookup"><span data-stu-id="12ff5-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="12ff5-113">Pierwsze polecenie uzyskuje zasób o nazwie ContosoSite przy użyciu polecenia cmdlet Get-AzureRmResource, a następnie zapisuje go w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="12ff5-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="12ff5-114">Drugie polecenie modyfikuje Właściwość $Resource.</span><span class="sxs-lookup"><span data-stu-id="12ff5-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="12ff5-115">Polecenie ostatnie powoduje zaktualizowanie zasobu w celu dopasowania $Resource.</span><span class="sxs-lookup"><span data-stu-id="12ff5-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="12ff5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12ff5-116">PARAMETERS</span></span>

### <span data-ttu-id="12ff5-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12ff5-117">-ApiVersion</span></span>
<span data-ttu-id="12ff5-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="12ff5-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="12ff5-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="12ff5-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="12ff5-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="12ff5-120">-ExtensionResourceName</span></span>
<span data-ttu-id="12ff5-121">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="12ff5-122">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="12ff5-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="12ff5-123">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="12ff5-123">server name`/`database name</span></span>

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

### <span data-ttu-id="12ff5-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="12ff5-124">-ExtensionResourceType</span></span>
<span data-ttu-id="12ff5-125">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="12ff5-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="12ff5-126">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="12ff5-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="12ff5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="12ff5-127">-Force</span></span>
<span data-ttu-id="12ff5-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="12ff5-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12ff5-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="12ff5-129">-Kind</span></span>
<span data-ttu-id="12ff5-130">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="12ff5-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="12ff5-131">-ODataQuery</span></span>
<span data-ttu-id="12ff5-132">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="12ff5-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="12ff5-133">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="12ff5-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="12ff5-134">-Plan</span><span class="sxs-lookup"><span data-stu-id="12ff5-134">-Plan</span></span>
<span data-ttu-id="12ff5-135">Określa właściwości planu zasobów jako tabelę skrótów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="12ff5-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="12ff5-136">-Pre</span></span>
<span data-ttu-id="12ff5-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="12ff5-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="12ff5-138">-Properties</span><span class="sxs-lookup"><span data-stu-id="12ff5-138">-Properties</span></span>
<span data-ttu-id="12ff5-139">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="12ff5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ff5-140">-ResourceGroupName</span></span>
<span data-ttu-id="12ff5-141">Określa nazwę grupy zasobów, w której to polecenie cmdlet modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="12ff5-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="12ff5-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ff5-142">-ResourceId</span></span>
<span data-ttu-id="12ff5-143">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="12ff5-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="12ff5-144">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="12ff5-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="12ff5-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="12ff5-145">-ResourceName</span></span>
<span data-ttu-id="12ff5-146">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="12ff5-147">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="12ff5-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="12ff5-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="12ff5-148">-ResourceType</span></span>
<span data-ttu-id="12ff5-149">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="12ff5-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="12ff5-150">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="12ff5-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="12ff5-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="12ff5-151">-Sku</span></span>
<span data-ttu-id="12ff5-152">Określa obiekt SKU zasobu jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="12ff5-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="12ff5-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="12ff5-153">-Tag</span></span>
<span data-ttu-id="12ff5-154">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="12ff5-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12ff5-155">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="12ff5-155">For example:</span></span>

<span data-ttu-id="12ff5-156">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="12ff5-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="12ff5-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="12ff5-157">-TenantLevel</span></span>
<span data-ttu-id="12ff5-158">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="12ff5-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="12ff5-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="12ff5-159">-UsePatchSemantics</span></span>
<span data-ttu-id="12ff5-160">Wskazuje, że w tym poleceniu cmdlet jest używana poprawka HTTP w celu zaktualizowania obiektu zamiast funkcji PUT HTTP.</span><span class="sxs-lookup"><span data-stu-id="12ff5-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="12ff5-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12ff5-161">-Confirm</span></span>
<span data-ttu-id="12ff5-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ff5-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ff5-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ff5-163">-WhatIf</span></span>
<span data-ttu-id="12ff5-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ff5-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ff5-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12ff5-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ff5-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ff5-166">-DefaultProfile</span></span>
<span data-ttu-id="12ff5-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12ff5-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12ff5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ff5-168">CommonParameters</span></span>
<span data-ttu-id="12ff5-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ff5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ff5-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ff5-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ff5-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12ff5-171">INPUTS</span></span>

## <span data-ttu-id="12ff5-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12ff5-172">OUTPUTS</span></span>

### <span data-ttu-id="12ff5-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="12ff5-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="12ff5-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12ff5-174">NOTES</span></span>

## <span data-ttu-id="12ff5-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12ff5-175">RELATED LINKS</span></span>

[<span data-ttu-id="12ff5-176">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="12ff5-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="12ff5-178">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="12ff5-179">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="12ff5-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ff5-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
