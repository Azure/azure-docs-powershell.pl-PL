---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201954"
---
# <span data-ttu-id="24e60-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="24e60-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="24e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e60-102">SYNOPSIS</span></span>
<span data-ttu-id="24e60-103">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="24e60-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="24e60-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24e60-104">SYNTAX</span></span>

### <span data-ttu-id="24e60-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="24e60-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24e60-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24e60-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24e60-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="24e60-107">DESCRIPTION</span></span>
<span data-ttu-id="24e60-108">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="24e60-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="24e60-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24e60-109">EXAMPLES</span></span>

### <span data-ttu-id="24e60-110">Przykład 1. Usunięcie pamięci podręcznej Redis Enterprise Cache i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="24e60-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="24e60-111">To polecenie usuwa pamięć podręczną Redis Enterprise Cache i wyświetla, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="24e60-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="24e60-112">Przykład 2. Usunięcie pamięci podręcznej Redis Enterprise Cache i nie wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="24e60-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="24e60-113">To polecenie usuwa pamięć podręczną redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="24e60-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="24e60-114">Parametr PassThru nie jest określony, dlatego wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="24e60-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="24e60-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24e60-115">PARAMETERS</span></span>

### <span data-ttu-id="24e60-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="24e60-116">-AsJob</span></span>
<span data-ttu-id="24e60-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="24e60-117">Run the command as a job</span></span>

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

### <span data-ttu-id="24e60-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="24e60-118">-ClusterName</span></span>
<span data-ttu-id="24e60-119">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="24e60-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e60-120">-DefaultProfile</span></span>
<span data-ttu-id="24e60-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24e60-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e60-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24e60-122">-InputObject</span></span>
<span data-ttu-id="24e60-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="24e60-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24e60-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24e60-124">-NoWait</span></span>
<span data-ttu-id="24e60-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="24e60-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24e60-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24e60-126">-PassThru</span></span>
<span data-ttu-id="24e60-127">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="24e60-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="24e60-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e60-128">-ResourceGroupName</span></span>
<span data-ttu-id="24e60-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24e60-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="24e60-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24e60-130">-SubscriptionId</span></span>
<span data-ttu-id="24e60-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24e60-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="24e60-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="24e60-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24e60-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24e60-133">-Confirm</span></span>
<span data-ttu-id="24e60-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24e60-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e60-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e60-135">-WhatIf</span></span>
<span data-ttu-id="24e60-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e60-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e60-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24e60-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e60-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e60-138">CommonParameters</span></span>
<span data-ttu-id="24e60-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e60-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e60-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24e60-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e60-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e60-141">INPUTS</span></span>

### <span data-ttu-id="24e60-142">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="24e60-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="24e60-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e60-143">OUTPUTS</span></span>

### <span data-ttu-id="24e60-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24e60-144">System.Boolean</span></span>

## <span data-ttu-id="24e60-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24e60-145">NOTES</span></span>

<span data-ttu-id="24e60-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="24e60-146">ALIASES</span></span>

<span data-ttu-id="24e60-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24e60-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24e60-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="24e60-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24e60-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24e60-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24e60-150">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="24e60-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24e60-151">`[ClusterName <String>]`: nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="24e60-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="24e60-152">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="24e60-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="24e60-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="24e60-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24e60-154">`[Location <String>]`: region, w który znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="24e60-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="24e60-155">`[OperationId <String>]`: czas trwania identyfikator unikatowy.</span><span class="sxs-lookup"><span data-stu-id="24e60-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="24e60-156">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="24e60-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="24e60-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24e60-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="24e60-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24e60-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="24e60-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="24e60-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="24e60-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24e60-160">RELATED LINKS</span></span>

