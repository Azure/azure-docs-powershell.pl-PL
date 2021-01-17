---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327950"
---
# <span data-ttu-id="e2585-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="e2585-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="e2585-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2585-102">SYNOPSIS</span></span>
<span data-ttu-id="e2585-103">Umożliwia wywołanie akcji dotyczącej zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2585-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="e2585-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2585-104">SYNTAX</span></span>

### <span data-ttu-id="e2585-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2585-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2585-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e2585-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2585-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e2585-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2585-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2585-108">DESCRIPTION</span></span>
<span data-ttu-id="e2585-109">Polecenie cmdlet **Invoke-AzResourceAction** umożliwia wywołanie akcji dotyczącej określonego zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2585-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="e2585-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Eksplorator zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2585-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="e2585-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2585-111">EXAMPLES</span></span>

### <span data-ttu-id="e2585-112">Przykład 1: wywoływanie Rozpoczynanie maszyny wirtualnej z identyfikatorem ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2585-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e2585-113">To polecenie umożliwia uruchomienie maszyny wirtualnej z identyfikatorem {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="e2585-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="e2585-114">Przykład 2: wywołanie maszyny wirtualnej z resourceName poweroffing</span><span class="sxs-lookup"><span data-stu-id="e2585-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="e2585-115">To polecenie zatrzymuje maszynę wirtualną za pomocą {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="e2585-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="e2585-116">Polecenie określa parametr *Force* , dlatego nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2585-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e2585-117">Przykład 3: wywoływanie rejestrowania dostawcy zasobów z identyfikatorem ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2585-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

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

<span data-ttu-id="e2585-118">To polecenie rejestruje dostawcę zasobów "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="e2585-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="e2585-119">Polecenie określa parametr *Force* , dlatego nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2585-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e2585-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2585-120">PARAMETERS</span></span>

### <span data-ttu-id="e2585-121">-Action</span><span class="sxs-lookup"><span data-stu-id="e2585-121">-Action</span></span>
<span data-ttu-id="e2585-122">Określa nazwę akcji, którą należy wywołać.</span><span class="sxs-lookup"><span data-stu-id="e2585-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="e2585-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2585-123">-ApiVersion</span></span>
<span data-ttu-id="e2585-124">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e2585-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2585-125">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="e2585-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e2585-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2585-126">-DefaultProfile</span></span>
<span data-ttu-id="e2585-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e2585-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2585-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e2585-128">-ExtensionResourceName</span></span>
<span data-ttu-id="e2585-129">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="e2585-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="e2585-130">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="e2585-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e2585-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e2585-131">-ExtensionResourceType</span></span>
<span data-ttu-id="e2585-132">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e2585-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="e2585-133">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e2585-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e2585-134">-Force</span><span class="sxs-lookup"><span data-stu-id="e2585-134">-Force</span></span>
<span data-ttu-id="e2585-135">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e2585-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2585-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e2585-136">-ODataQuery</span></span>
<span data-ttu-id="e2585-137">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e2585-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e2585-138">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="e2585-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e2585-139">— Parametry</span><span class="sxs-lookup"><span data-stu-id="e2585-139">-Parameters</span></span>
<span data-ttu-id="e2585-140">Określa parametry jako tabelę skrótów dla akcji, która wywołuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2585-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="e2585-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2585-141">-Pre</span></span>
<span data-ttu-id="e2585-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e2585-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2585-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2585-143">-ResourceGroupName</span></span>
<span data-ttu-id="e2585-144">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="e2585-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="e2585-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2585-145">-ResourceId</span></span>
<span data-ttu-id="e2585-146">Określa w pełni kwalifikowany identyfikator zasobu dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="e2585-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="e2585-147">Identyfikator zawiera abonament, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e2585-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e2585-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e2585-148">-ResourceName</span></span>
<span data-ttu-id="e2585-149">Określa nazwę zasobu zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="e2585-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="e2585-150">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e2585-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e2585-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e2585-151">-ResourceType</span></span>
<span data-ttu-id="e2585-152">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2585-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="e2585-153">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e2585-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e2585-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e2585-154">-TenantLevel</span></span>
<span data-ttu-id="e2585-155">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e2585-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e2585-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2585-156">-Confirm</span></span>
<span data-ttu-id="e2585-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2585-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2585-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2585-158">-WhatIf</span></span>
<span data-ttu-id="e2585-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2585-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2585-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2585-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2585-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2585-161">CommonParameters</span></span>
<span data-ttu-id="e2585-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2585-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2585-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2585-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2585-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2585-164">INPUTS</span></span>

### <span data-ttu-id="e2585-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e2585-165">System.String</span></span>

## <span data-ttu-id="e2585-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2585-166">OUTPUTS</span></span>

### <span data-ttu-id="e2585-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e2585-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e2585-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2585-168">NOTES</span></span>

## <span data-ttu-id="e2585-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2585-169">RELATED LINKS</span></span>
