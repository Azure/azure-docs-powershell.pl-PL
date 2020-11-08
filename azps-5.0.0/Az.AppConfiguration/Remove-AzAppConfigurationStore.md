---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225411"
---
# <span data-ttu-id="ea1d0-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="ea1d0-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="ea1d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1d0-103">Usuwa magazyn konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="ea1d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea1d0-104">SYNTAX</span></span>

### <span data-ttu-id="ea1d0-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ea1d0-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea1d0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea1d0-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea1d0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea1d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ea1d0-108">Usuwa magazyn konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="ea1d0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea1d0-109">EXAMPLES</span></span>

### <span data-ttu-id="ea1d0-110">Przykład 1: Usuwanie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="ea1d0-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="ea1d0-111">To polecenie umożliwia usunięcie magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="ea1d0-112">Przykład 2: Usuwanie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="ea1d0-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="ea1d0-113">To polecenie umożliwia usunięcie magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="ea1d0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea1d0-114">PARAMETERS</span></span>

### <span data-ttu-id="ea1d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea1d0-115">-AsJob</span></span>
<span data-ttu-id="ea1d0-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ea1d0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ea1d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1d0-117">-DefaultProfile</span></span>
<span data-ttu-id="ea1d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea1d0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea1d0-119">-InputObject</span></span>
<span data-ttu-id="ea1d0-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea1d0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea1d0-121">-Name</span></span>
<span data-ttu-id="ea1d0-122">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="ea1d0-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ea1d0-123">-NoWait</span></span>
<span data-ttu-id="ea1d0-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ea1d0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea1d0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea1d0-125">-PassThru</span></span>
<span data-ttu-id="ea1d0-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ea1d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea1d0-128">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="ea1d0-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ea1d0-129">-SubscriptionId</span></span>
<span data-ttu-id="ea1d0-130">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="ea1d0-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea1d0-131">-Confirm</span></span>
<span data-ttu-id="ea1d0-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1d0-133">-WhatIf</span></span>
<span data-ttu-id="ea1d0-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1d0-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1d0-136">CommonParameters</span></span>
<span data-ttu-id="ea1d0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1d0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1d0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1d0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea1d0-139">INPUTS</span></span>

### <span data-ttu-id="ea1d0-140">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="ea1d0-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="ea1d0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea1d0-141">OUTPUTS</span></span>

### <span data-ttu-id="ea1d0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea1d0-142">System.Boolean</span></span>

## <span data-ttu-id="ea1d0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea1d0-143">NOTES</span></span>

<span data-ttu-id="ea1d0-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ea1d0-144">ALIASES</span></span>

<span data-ttu-id="ea1d0-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea1d0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea1d0-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea1d0-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea1d0-148">INPUTobject <IAppConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ea1d0-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea1d0-149">`[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="ea1d0-150">`[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="ea1d0-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ea1d0-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea1d0-152">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ea1d0-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="ea1d0-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="ea1d0-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1d0-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="ea1d0-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea1d0-155">RELATED LINKS</span></span>

