---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 31039d71f0c26b6fea3e19220b3932d2abd02073
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242482"
---
# <span data-ttu-id="95e29-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e29-101">Remove-AzResource</span></span>

## <span data-ttu-id="95e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e29-102">SYNOPSIS</span></span>
<span data-ttu-id="95e29-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="95e29-103">Removes a resource.</span></span>

## <span data-ttu-id="95e29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95e29-104">SYNTAX</span></span>

### <span data-ttu-id="95e29-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="95e29-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e29-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="95e29-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95e29-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="95e29-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e29-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="95e29-108">DESCRIPTION</span></span>
<span data-ttu-id="95e29-109">Polecenie **cmdlet Remove-AzResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95e29-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="95e29-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95e29-110">EXAMPLES</span></span>

### <span data-ttu-id="95e29-111">Przykład 1. Usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="95e29-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="95e29-112">To polecenie usuwa zasób witryny sieci Web o nazwie Witryna Contoso.</span><span class="sxs-lookup"><span data-stu-id="95e29-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="95e29-113">W tym przykładzie użyto wartości zastępczej identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="95e29-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="95e29-114">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="95e29-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="95e29-115">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95e29-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="95e29-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95e29-116">PARAMETERS</span></span>

### <span data-ttu-id="95e29-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="95e29-117">-ApiVersion</span></span>
<span data-ttu-id="95e29-118">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="95e29-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="95e29-119">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="95e29-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="95e29-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="95e29-120">-AsJob</span></span>
<span data-ttu-id="95e29-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="95e29-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95e29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e29-122">-DefaultProfile</span></span>
<span data-ttu-id="95e29-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="95e29-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95e29-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="95e29-124">-ExtensionResourceName</span></span>
<span data-ttu-id="95e29-125">Określa nazwę zasobu rozszerzenia, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e29-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="95e29-126">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa bazy danych o `/` nazwie serwera</span><span class="sxs-lookup"><span data-stu-id="95e29-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="95e29-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="95e29-127">-ExtensionResourceType</span></span>
<span data-ttu-id="95e29-128">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="95e29-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="95e29-129">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="95e29-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="95e29-130">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="95e29-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="95e29-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="95e29-131">-Force</span></span>
<span data-ttu-id="95e29-132">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="95e29-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95e29-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="95e29-133">-ODataQuery</span></span>
<span data-ttu-id="95e29-134">Określa filtr stylu protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="95e29-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="95e29-135">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="95e29-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="95e29-136">— Przed</span><span class="sxs-lookup"><span data-stu-id="95e29-136">-Pre</span></span>
<span data-ttu-id="95e29-137">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="95e29-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="95e29-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e29-138">-ResourceGroupName</span></span>
<span data-ttu-id="95e29-139">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="95e29-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="95e29-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95e29-140">-ResourceId</span></span>
<span data-ttu-id="95e29-141">Określa w pełni kwalifikowany identyfikator zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e29-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="95e29-142">Identyfikator obejmuje subskrypcję, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="95e29-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="95e29-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="95e29-143">-ResourceName</span></span>
<span data-ttu-id="95e29-144">Określa nazwę zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e29-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="95e29-145">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="95e29-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="95e29-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="95e29-146">-ResourceType</span></span>
<span data-ttu-id="95e29-147">Określa typ zasobu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e29-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="95e29-148">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="95e29-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="95e29-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="95e29-149">-TenantLevel</span></span>
<span data-ttu-id="95e29-150">Wskazuje, że to polecenie cmdlet działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="95e29-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="95e29-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95e29-151">-Confirm</span></span>
<span data-ttu-id="95e29-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95e29-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e29-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e29-153">-WhatIf</span></span>
<span data-ttu-id="95e29-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e29-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e29-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95e29-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e29-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e29-156">CommonParameters</span></span>
<span data-ttu-id="95e29-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e29-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e29-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95e29-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e29-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95e29-159">INPUTS</span></span>

### <span data-ttu-id="95e29-160">System.String</span><span class="sxs-lookup"><span data-stu-id="95e29-160">System.String</span></span>

## <span data-ttu-id="95e29-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95e29-161">OUTPUTS</span></span>

### <span data-ttu-id="95e29-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95e29-162">System.Boolean</span></span>

## <span data-ttu-id="95e29-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95e29-163">NOTES</span></span>

## <span data-ttu-id="95e29-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95e29-164">RELATED LINKS</span></span>

[<span data-ttu-id="95e29-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e29-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="95e29-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e29-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="95e29-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e29-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="95e29-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e29-168">Set-AzResource</span></span>](./Set-AzResource.md)


