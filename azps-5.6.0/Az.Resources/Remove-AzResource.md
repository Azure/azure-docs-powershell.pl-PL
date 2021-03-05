---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 6d2dd13f08fd9e621f30f586e7c46c828387e31e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963770"
---
# <span data-ttu-id="45b72-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="45b72-101">Remove-AzResource</span></span>

## <span data-ttu-id="45b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b72-102">SYNOPSIS</span></span>
<span data-ttu-id="45b72-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="45b72-103">Removes a resource.</span></span>

## <span data-ttu-id="45b72-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45b72-104">SYNTAX</span></span>

### <span data-ttu-id="45b72-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="45b72-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b72-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="45b72-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45b72-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="45b72-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b72-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="45b72-108">DESCRIPTION</span></span>
<span data-ttu-id="45b72-109">Polecenie **cmdlet Remove-AzResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="45b72-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="45b72-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45b72-110">EXAMPLES</span></span>

### <span data-ttu-id="45b72-111">Przykład 1. Usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="45b72-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="45b72-112">To polecenie usuwa zasób witryny sieci Web o nazwie Witryna Contoso.</span><span class="sxs-lookup"><span data-stu-id="45b72-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="45b72-113">W przykładzie użyto wartości zastępczej identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="45b72-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="45b72-114">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="45b72-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="45b72-115">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45b72-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="45b72-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45b72-116">PARAMETERS</span></span>

### <span data-ttu-id="45b72-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="45b72-117">-ApiVersion</span></span>
<span data-ttu-id="45b72-118">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="45b72-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="45b72-119">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="45b72-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="45b72-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="45b72-120">-AsJob</span></span>
<span data-ttu-id="45b72-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="45b72-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45b72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b72-122">-DefaultProfile</span></span>
<span data-ttu-id="45b72-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="45b72-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45b72-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="45b72-124">-ExtensionResourceName</span></span>
<span data-ttu-id="45b72-125">Określa nazwę zasobu rozszerzenia, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="45b72-126">Aby na przykład określić bazę danych, należy użyć następującego formatu: nazwa bazy danych o `/` nazwie serwera.</span><span class="sxs-lookup"><span data-stu-id="45b72-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="45b72-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="45b72-127">-ExtensionResourceType</span></span>
<span data-ttu-id="45b72-128">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="45b72-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="45b72-129">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="45b72-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="45b72-130">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="45b72-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="45b72-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="45b72-131">-Force</span></span>
<span data-ttu-id="45b72-132">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45b72-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45b72-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="45b72-133">-ODataQuery</span></span>
<span data-ttu-id="45b72-134">Określa filtr stylu protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="45b72-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="45b72-135">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="45b72-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="45b72-136">— Przed</span><span class="sxs-lookup"><span data-stu-id="45b72-136">-Pre</span></span>
<span data-ttu-id="45b72-137">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="45b72-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="45b72-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b72-138">-ResourceGroupName</span></span>
<span data-ttu-id="45b72-139">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="45b72-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="45b72-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b72-140">-ResourceId</span></span>
<span data-ttu-id="45b72-141">Określa w pełni kwalifikowany identyfikator zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="45b72-142">Identyfikator obejmuje subskrypcję, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="45b72-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="45b72-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="45b72-143">-ResourceName</span></span>
<span data-ttu-id="45b72-144">Określa nazwę zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="45b72-145">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="45b72-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="45b72-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="45b72-146">-ResourceType</span></span>
<span data-ttu-id="45b72-147">Określa typ zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="45b72-148">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="45b72-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="45b72-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="45b72-149">-TenantLevel</span></span>
<span data-ttu-id="45b72-150">Wskazuje, że to polecenie cmdlet działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="45b72-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="45b72-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45b72-151">-Confirm</span></span>
<span data-ttu-id="45b72-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45b72-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b72-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b72-153">-WhatIf</span></span>
<span data-ttu-id="45b72-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b72-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="45b72-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b72-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b72-156">CommonParameters</span></span>
<span data-ttu-id="45b72-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b72-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b72-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45b72-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b72-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b72-159">INPUTS</span></span>

### <span data-ttu-id="45b72-160">System.String</span><span class="sxs-lookup"><span data-stu-id="45b72-160">System.String</span></span>

## <span data-ttu-id="45b72-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b72-161">OUTPUTS</span></span>

### <span data-ttu-id="45b72-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45b72-162">System.Boolean</span></span>

## <span data-ttu-id="45b72-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45b72-163">NOTES</span></span>

## <span data-ttu-id="45b72-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b72-164">RELATED LINKS</span></span>

[<span data-ttu-id="45b72-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="45b72-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="45b72-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="45b72-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="45b72-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="45b72-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="45b72-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="45b72-168">Set-AzResource</span></span>](./Set-AzResource.md)


