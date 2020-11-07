---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718470"
---
# <span data-ttu-id="ef119-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="ef119-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef119-102">SYNOPSIS</span></span>
<span data-ttu-id="ef119-103">Modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="ef119-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef119-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef119-104">SYNTAX</span></span>

### <span data-ttu-id="ef119-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef119-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef119-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ef119-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef119-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef119-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef119-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ef119-108">DESCRIPTION</span></span>
<span data-ttu-id="ef119-109">Polecenie cmdlet **Set-AzureRmResource** modyfikuje istniejący zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef119-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="ef119-110">Określ zasób do zmodyfikowania według nazwy i typu lub według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="ef119-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="ef119-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef119-111">EXAMPLES</span></span>

### <span data-ttu-id="ef119-112">Przykład 1. Modyfikowanie zasobu</span><span class="sxs-lookup"><span data-stu-id="ef119-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="ef119-113">Pierwsze polecenie uzyskuje zasób o nazwie ContosoSite przy użyciu polecenia cmdlet Get-AzureRmResource, a następnie zapisuje go w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="ef119-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="ef119-114">Drugie polecenie modyfikuje Właściwość $Resource.</span><span class="sxs-lookup"><span data-stu-id="ef119-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="ef119-115">Polecenie ostatnie powoduje zaktualizowanie zasobu w celu dopasowania $Resource.</span><span class="sxs-lookup"><span data-stu-id="ef119-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="ef119-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef119-116">PARAMETERS</span></span>

### <span data-ttu-id="ef119-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef119-117">-ApiVersion</span></span>
<span data-ttu-id="ef119-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ef119-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef119-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="ef119-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef119-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef119-120">-AsJob</span></span>
<span data-ttu-id="ef119-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ef119-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef119-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef119-122">-DefaultProfile</span></span>
<span data-ttu-id="ef119-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ef119-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef119-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ef119-124">-ExtensionResourceName</span></span>
<span data-ttu-id="ef119-125">Określa nazwę zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="ef119-126">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="ef119-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="ef119-127">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="ef119-127">server name`/`database name</span></span>

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

### <span data-ttu-id="ef119-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ef119-128">-ExtensionResourceType</span></span>
<span data-ttu-id="ef119-129">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ef119-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="ef119-130">Jeśli na przykład zasób rozszerzenia jest bazą danych, określ następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="ef119-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="ef119-131">-Force</span><span class="sxs-lookup"><span data-stu-id="ef119-131">-Force</span></span>
<span data-ttu-id="ef119-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ef119-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef119-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="ef119-133">-Kind</span></span>
<span data-ttu-id="ef119-134">Określa rodzaj zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef119-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ef119-135">-ODataQuery</span></span>
<span data-ttu-id="ef119-136">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef119-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ef119-137">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="ef119-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ef119-138">-Plan</span><span class="sxs-lookup"><span data-stu-id="ef119-138">-Plan</span></span>
<span data-ttu-id="ef119-139">Określa właściwości planu zasobów jako tabelę skrótów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef119-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef119-140">-Pre</span></span>
<span data-ttu-id="ef119-141">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ef119-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef119-142">-Properties</span><span class="sxs-lookup"><span data-stu-id="ef119-142">-Properties</span></span>
<span data-ttu-id="ef119-143">Określa właściwości zasobu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef119-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef119-144">-ResourceGroupName</span></span>
<span data-ttu-id="ef119-145">Określa nazwę grupy zasobów, w której to polecenie cmdlet modyfikuje zasób.</span><span class="sxs-lookup"><span data-stu-id="ef119-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="ef119-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef119-146">-ResourceId</span></span>
<span data-ttu-id="ef119-147">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="ef119-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="ef119-148">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ef119-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ef119-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef119-149">-ResourceName</span></span>
<span data-ttu-id="ef119-150">Określa nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="ef119-151">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="ef119-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="ef119-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef119-152">-ResourceType</span></span>
<span data-ttu-id="ef119-153">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef119-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="ef119-154">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="ef119-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="ef119-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="ef119-155">-Sku</span></span>
<span data-ttu-id="ef119-156">Określa obiekt SKU zasobu jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ef119-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="ef119-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef119-157">-Tag</span></span>
<span data-ttu-id="ef119-158">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ef119-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef119-159">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="ef119-159">For example:</span></span>

<span data-ttu-id="ef119-160">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ef119-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef119-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef119-161">-TenantLevel</span></span>
<span data-ttu-id="ef119-162">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef119-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ef119-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="ef119-163">-UsePatchSemantics</span></span>
<span data-ttu-id="ef119-164">Wskazuje, że w tym poleceniu cmdlet jest używana poprawka HTTP w celu zaktualizowania obiektu zamiast funkcji PUT HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef119-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="ef119-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef119-165">-Confirm</span></span>
<span data-ttu-id="ef119-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef119-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef119-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef119-167">-WhatIf</span></span>
<span data-ttu-id="ef119-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef119-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef119-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef119-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef119-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef119-170">CommonParameters</span></span>
<span data-ttu-id="ef119-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef119-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef119-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef119-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef119-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef119-173">INPUTS</span></span>

### <span data-ttu-id="ef119-174">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ef119-174">None</span></span>
<span data-ttu-id="ef119-175">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ef119-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef119-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef119-176">OUTPUTS</span></span>

### <span data-ttu-id="ef119-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ef119-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ef119-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef119-178">NOTES</span></span>

## <span data-ttu-id="ef119-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef119-179">RELATED LINKS</span></span>

[<span data-ttu-id="ef119-180">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="ef119-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ef119-182">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ef119-183">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ef119-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef119-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
