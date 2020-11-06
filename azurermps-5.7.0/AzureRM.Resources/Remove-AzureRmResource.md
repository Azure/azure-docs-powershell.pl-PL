---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548000"
---
# <span data-ttu-id="e4dbd-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="e4dbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dbd-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4dbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4dbd-104">SYNTAX</span></span>

### <span data-ttu-id="e4dbd-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4dbd-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4dbd-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e4dbd-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4dbd-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e4dbd-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4dbd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="e4dbd-109">Polecenie cmdlet **Remove-AzureRmResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="e4dbd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="e4dbd-111">Przykład 1: usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="e4dbd-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="e4dbd-112">To polecenie usuwa zasób witryny sieci Web o nazwie ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="e4dbd-113">W przykładzie użyto wartości zastępczej dla identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="e4dbd-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="e4dbd-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e4dbd-115">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e4dbd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4dbd-116">PARAMETERS</span></span>

### <span data-ttu-id="e4dbd-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4dbd-117">-ApiVersion</span></span>
<span data-ttu-id="e4dbd-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e4dbd-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e4dbd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4dbd-120">-AsJob</span></span>
<span data-ttu-id="e4dbd-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e4dbd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4dbd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dbd-122">-DefaultProfile</span></span>
<span data-ttu-id="e4dbd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4dbd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4dbd-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e4dbd-124">-ExtensionResourceName</span></span>
<span data-ttu-id="e4dbd-125">Określa nazwę zasobu rozszerzenia zasobu, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e4dbd-126">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="e4dbd-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="e4dbd-127">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="e4dbd-127">server name`/`database name</span></span>

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

### <span data-ttu-id="e4dbd-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e4dbd-128">-ExtensionResourceType</span></span>
<span data-ttu-id="e4dbd-129">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e4dbd-130">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="e4dbd-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e4dbd-131">For instance:</span></span> 

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

### <span data-ttu-id="e4dbd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e4dbd-132">-Force</span></span>
<span data-ttu-id="e4dbd-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4dbd-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e4dbd-134">-ODataQuery</span></span>
<span data-ttu-id="e4dbd-135">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e4dbd-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e4dbd-136">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e4dbd-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="e4dbd-137">-Pre</span></span>
<span data-ttu-id="e4dbd-138">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4dbd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4dbd-139">-ResourceGroupName</span></span>
<span data-ttu-id="e4dbd-140">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="e4dbd-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4dbd-141">-ResourceId</span></span>
<span data-ttu-id="e4dbd-142">Określa w pełni kwalifikowany identyfikator zasobu, którego usunięcie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e4dbd-143">Identyfikator zawiera abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="e4dbd-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="e4dbd-144">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e4dbd-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e4dbd-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e4dbd-145">-ResourceName</span></span>
<span data-ttu-id="e4dbd-146">Określa nazwę zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e4dbd-147">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="e4dbd-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="e4dbd-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e4dbd-148">-ResourceType</span></span>
<span data-ttu-id="e4dbd-149">Określa typ zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e4dbd-150">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="e4dbd-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="e4dbd-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e4dbd-151">-TenantLevel</span></span>
<span data-ttu-id="e4dbd-152">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e4dbd-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4dbd-153">-Confirm</span></span>
<span data-ttu-id="e4dbd-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4dbd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4dbd-155">-WhatIf</span></span>
<span data-ttu-id="e4dbd-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4dbd-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4dbd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dbd-158">CommonParameters</span></span>
<span data-ttu-id="e4dbd-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dbd-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4dbd-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dbd-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4dbd-161">INPUTS</span></span>

### <span data-ttu-id="e4dbd-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e4dbd-162">None</span></span>
<span data-ttu-id="e4dbd-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e4dbd-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4dbd-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4dbd-164">OUTPUTS</span></span>

### <span data-ttu-id="e4dbd-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4dbd-165">System.Boolean</span></span>

## <span data-ttu-id="e4dbd-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4dbd-166">NOTES</span></span>

## <span data-ttu-id="e4dbd-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4dbd-167">RELATED LINKS</span></span>

[<span data-ttu-id="e4dbd-168">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="e4dbd-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="e4dbd-170">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e4dbd-171">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e4dbd-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4dbd-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


