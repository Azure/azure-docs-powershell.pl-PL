---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182298"
---
# <span data-ttu-id="8885d-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8885d-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="8885d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8885d-102">SYNOPSIS</span></span>
<span data-ttu-id="8885d-103">Usuwa magazyn konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8885d-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="8885d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8885d-104">SYNTAX</span></span>

### <span data-ttu-id="8885d-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="8885d-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8885d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8885d-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8885d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8885d-107">DESCRIPTION</span></span>
<span data-ttu-id="8885d-108">Usuwa magazyn konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8885d-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="8885d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8885d-109">EXAMPLES</span></span>

### <span data-ttu-id="8885d-110">Przykład 1. Usuwanie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="8885d-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="8885d-111">To polecenie usuwa magazyn konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8885d-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="8885d-112">Przykład 2. Usuwanie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="8885d-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="8885d-113">To polecenie usuwa magazyn konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8885d-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="8885d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8885d-114">PARAMETERS</span></span>

### <span data-ttu-id="8885d-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8885d-115">-AsJob</span></span>
<span data-ttu-id="8885d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8885d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8885d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8885d-117">-DefaultProfile</span></span>
<span data-ttu-id="8885d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8885d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8885d-119">-InputObject</span></span>
<span data-ttu-id="8885d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8885d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8885d-121">-Name</span></span>
<span data-ttu-id="8885d-122">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8885d-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8885d-123">-NoWait</span></span>
<span data-ttu-id="8885d-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8885d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8885d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8885d-125">-PassThru</span></span>
<span data-ttu-id="8885d-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8885d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8885d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8885d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8885d-128">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="8885d-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8885d-129">-SubscriptionId</span></span>
<span data-ttu-id="8885d-130">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8885d-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8885d-131">-Confirm</span></span>
<span data-ttu-id="8885d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8885d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8885d-133">-WhatIf</span></span>
<span data-ttu-id="8885d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8885d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8885d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8885d-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8885d-136">CommonParameters</span></span>
<span data-ttu-id="8885d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8885d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8885d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8885d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8885d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8885d-139">INPUTS</span></span>

### <span data-ttu-id="8885d-140">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="8885d-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="8885d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8885d-141">OUTPUTS</span></span>

### <span data-ttu-id="8885d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8885d-142">System.Boolean</span></span>

## <span data-ttu-id="8885d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8885d-143">NOTES</span></span>

<span data-ttu-id="8885d-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8885d-144">ALIASES</span></span>

<span data-ttu-id="8885d-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8885d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8885d-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8885d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8885d-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8885d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8885d-148">INPUTOBJECT: <IAppConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8885d-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8885d-149">`[ConfigStoreName <String>]`: nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8885d-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="8885d-150">`[GroupName <String>]`: nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="8885d-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="8885d-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8885d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8885d-152">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="8885d-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="8885d-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="8885d-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="8885d-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8885d-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="8885d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8885d-155">RELATED LINKS</span></span>

