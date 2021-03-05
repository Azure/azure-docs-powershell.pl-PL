---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 14da2ddfdd94be5cd95d00eeeb742b9e4ac982e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974465"
---
# <span data-ttu-id="73920-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="73920-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="73920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73920-102">SYNOPSIS</span></span>
<span data-ttu-id="73920-103">Wywołuje akcję na zasobie.</span><span class="sxs-lookup"><span data-stu-id="73920-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="73920-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73920-104">SYNTAX</span></span>

### <span data-ttu-id="73920-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="73920-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73920-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="73920-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73920-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="73920-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73920-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="73920-108">DESCRIPTION</span></span>
<span data-ttu-id="73920-109">Polecenie cmdlet **Invoke-AzResourceAction** wywołuje akcję dla określonego zasobu azure.</span><span class="sxs-lookup"><span data-stu-id="73920-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="73920-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Azure Resource Explorer.</span><span class="sxs-lookup"><span data-stu-id="73920-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="73920-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73920-111">EXAMPLES</span></span>

### <span data-ttu-id="73920-112">Przykład 1. Wywoływanie uruchamiania maszyny wirtualnej z argumentem ResourceId</span><span class="sxs-lookup"><span data-stu-id="73920-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="73920-113">To polecenie uruchamia maszynę wirtualną z {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="73920-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="73920-114">Przykład 2. Wywoływanie zasilania maszyny wirtualnej za pomocą nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="73920-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="73920-115">To polecenie zatrzymuje maszynę wirtualną za pomocą {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="73920-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="73920-116">Polecenie określa parametr *Force,* dlatego nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73920-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="73920-117">Przykład 3. Wywoływanie rejestrowania dostawcy zasobów u dostawcy resourceId</span><span class="sxs-lookup"><span data-stu-id="73920-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="73920-118">To polecenie rejestruje dostawcę zasobów "Microsoft.Network".</span><span class="sxs-lookup"><span data-stu-id="73920-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="73920-119">Polecenie określa parametr *Force,* dlatego nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73920-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="73920-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73920-120">PARAMETERS</span></span>

### <span data-ttu-id="73920-121">— Akcja</span><span class="sxs-lookup"><span data-stu-id="73920-121">-Action</span></span>
<span data-ttu-id="73920-122">Określa nazwę akcji, która ma być wywoływana.</span><span class="sxs-lookup"><span data-stu-id="73920-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73920-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="73920-123">-ApiVersion</span></span>
<span data-ttu-id="73920-124">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="73920-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="73920-125">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="73920-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="73920-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73920-126">-DefaultProfile</span></span>
<span data-ttu-id="73920-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="73920-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73920-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="73920-128">-ExtensionResourceName</span></span>
<span data-ttu-id="73920-129">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="73920-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="73920-130">Aby na przykład określić bazę danych, należy użyć następującego formatu: nazwa bazy danych o `/` nazwie serwera.</span><span class="sxs-lookup"><span data-stu-id="73920-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="73920-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="73920-131">-ExtensionResourceType</span></span>
<span data-ttu-id="73920-132">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="73920-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="73920-133">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="73920-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="73920-134">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="73920-134">-Force</span></span>
<span data-ttu-id="73920-135">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73920-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73920-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="73920-136">-ODataQuery</span></span>
<span data-ttu-id="73920-137">Określa filtr stylu protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="73920-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="73920-138">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="73920-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="73920-139">— Parametry</span><span class="sxs-lookup"><span data-stu-id="73920-139">-Parameters</span></span>
<span data-ttu-id="73920-140">Określa parametry, jako tabelę skrótów, dla akcji wywoływanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73920-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73920-141">— Przed</span><span class="sxs-lookup"><span data-stu-id="73920-141">-Pre</span></span>
<span data-ttu-id="73920-142">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="73920-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="73920-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73920-143">-ResourceGroupName</span></span>
<span data-ttu-id="73920-144">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="73920-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="73920-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73920-145">-ResourceId</span></span>
<span data-ttu-id="73920-146">Określa w pełni kwalifikowany identyfikator zasobu, do którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="73920-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="73920-147">Identyfikator obejmuje subskrypcję, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="73920-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="73920-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="73920-148">-ResourceName</span></span>
<span data-ttu-id="73920-149">Określa nazwę zasobu zasobu, do którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="73920-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="73920-150">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="73920-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="73920-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="73920-151">-ResourceType</span></span>
<span data-ttu-id="73920-152">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="73920-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="73920-153">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="73920-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="73920-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="73920-154">-TenantLevel</span></span>
<span data-ttu-id="73920-155">Wskazuje, że to polecenie cmdlet działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="73920-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="73920-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73920-156">-Confirm</span></span>
<span data-ttu-id="73920-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73920-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73920-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73920-158">-WhatIf</span></span>
<span data-ttu-id="73920-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73920-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73920-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73920-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73920-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73920-161">CommonParameters</span></span>
<span data-ttu-id="73920-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73920-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73920-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73920-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73920-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73920-164">INPUTS</span></span>

### <span data-ttu-id="73920-165">System.String</span><span class="sxs-lookup"><span data-stu-id="73920-165">System.String</span></span>

## <span data-ttu-id="73920-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73920-166">OUTPUTS</span></span>

### <span data-ttu-id="73920-167">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="73920-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="73920-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73920-168">NOTES</span></span>

## <span data-ttu-id="73920-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73920-169">RELATED LINKS</span></span>
