---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000737"
---
# <span data-ttu-id="eecaf-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="eecaf-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="eecaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eecaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eecaf-103">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="eecaf-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="eecaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eecaf-104">SYNTAX</span></span>

### <span data-ttu-id="eecaf-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="eecaf-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eecaf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eecaf-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eecaf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="eecaf-107">DESCRIPTION</span></span>
<span data-ttu-id="eecaf-108">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="eecaf-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="eecaf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eecaf-109">EXAMPLES</span></span>

### <span data-ttu-id="eecaf-110">Przykład 1. Usunięcie pamięci podręcznej Redis Enterprise Cache i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="eecaf-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="eecaf-111">To polecenie usuwa pamięć podręczną Redis Enterprise Cache i wyświetla, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="eecaf-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="eecaf-112">Przykład 2. Usunięcie pamięci podręcznej Redis Enterprise Cache i nie wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="eecaf-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="eecaf-113">To polecenie usuwa pamięć podręczną redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="eecaf-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="eecaf-114">Parametr PassThru nie jest określony, dlatego wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="eecaf-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="eecaf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eecaf-115">PARAMETERS</span></span>

### <span data-ttu-id="eecaf-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="eecaf-116">-AsJob</span></span>
<span data-ttu-id="eecaf-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="eecaf-117">Run the command as a job</span></span>

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

### <span data-ttu-id="eecaf-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eecaf-118">-ClusterName</span></span>
<span data-ttu-id="eecaf-119">Nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="eecaf-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="eecaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eecaf-120">-DefaultProfile</span></span>
<span data-ttu-id="eecaf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eecaf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eecaf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eecaf-122">-InputObject</span></span>
<span data-ttu-id="eecaf-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="eecaf-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eecaf-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eecaf-124">-NoWait</span></span>
<span data-ttu-id="eecaf-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="eecaf-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eecaf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eecaf-126">-PassThru</span></span>
<span data-ttu-id="eecaf-127">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="eecaf-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eecaf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eecaf-128">-ResourceGroupName</span></span>
<span data-ttu-id="eecaf-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eecaf-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="eecaf-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eecaf-130">-SubscriptionId</span></span>
<span data-ttu-id="eecaf-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eecaf-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="eecaf-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="eecaf-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eecaf-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eecaf-133">-Confirm</span></span>
<span data-ttu-id="eecaf-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eecaf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eecaf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eecaf-135">-WhatIf</span></span>
<span data-ttu-id="eecaf-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eecaf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eecaf-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eecaf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eecaf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eecaf-138">CommonParameters</span></span>
<span data-ttu-id="eecaf-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eecaf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eecaf-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eecaf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eecaf-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eecaf-141">INPUTS</span></span>

### <span data-ttu-id="eecaf-142">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="eecaf-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="eecaf-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eecaf-143">OUTPUTS</span></span>

### <span data-ttu-id="eecaf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eecaf-144">System.Boolean</span></span>

## <span data-ttu-id="eecaf-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eecaf-145">NOTES</span></span>

<span data-ttu-id="eecaf-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="eecaf-146">ALIASES</span></span>

<span data-ttu-id="eecaf-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eecaf-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eecaf-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="eecaf-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eecaf-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eecaf-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eecaf-150">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="eecaf-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eecaf-151">`[ClusterName <String>]`: nazwa klastra RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="eecaf-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="eecaf-152">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eecaf-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="eecaf-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="eecaf-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eecaf-154">`[Location <String>]`: region, w który znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="eecaf-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="eecaf-155">`[OperationId <String>]`: czas trwania identyfikator unikatowy.</span><span class="sxs-lookup"><span data-stu-id="eecaf-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="eecaf-156">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eecaf-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="eecaf-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eecaf-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="eecaf-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eecaf-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="eecaf-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="eecaf-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eecaf-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eecaf-160">RELATED LINKS</span></span>

