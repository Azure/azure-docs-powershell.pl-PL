---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378184"
---
# <span data-ttu-id="2a602-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="2a602-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="2a602-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a602-102">SYNOPSIS</span></span>
<span data-ttu-id="2a602-103">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2a602-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="2a602-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a602-104">SYNTAX</span></span>

### <span data-ttu-id="2a602-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2a602-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a602-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a602-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a602-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a602-107">DESCRIPTION</span></span>
<span data-ttu-id="2a602-108">Usuwa klaster pamięci podręcznej RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2a602-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="2a602-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a602-109">EXAMPLES</span></span>

### <span data-ttu-id="2a602-110">Przykład 1: usunięcie Redis pamięci podręcznej przedsiębiorstwa i zwrócenie wyniku</span><span class="sxs-lookup"><span data-stu-id="2a602-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="2a602-111">To polecenie usuwa Redis pamięci podręcznej przedsiębiorstwa i wyświetla, czy operacja jest udana.</span><span class="sxs-lookup"><span data-stu-id="2a602-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="2a602-112">Przykład 2: usunięcie Redis pamięci podręcznej przedsiębiorstwa i nie Wyświetlanie wyniku</span><span class="sxs-lookup"><span data-stu-id="2a602-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="2a602-113">To polecenie usuwa pamięć podręczną przedsiębiorstwa Redis.</span><span class="sxs-lookup"><span data-stu-id="2a602-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="2a602-114">Ponieważ parametr PassThru nie jest określony, wynik operacji nie jest wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="2a602-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="2a602-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a602-115">PARAMETERS</span></span>

### <span data-ttu-id="2a602-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a602-116">-AsJob</span></span>
<span data-ttu-id="2a602-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2a602-117">Run the command as a job</span></span>

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

### <span data-ttu-id="2a602-118">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2a602-118">-ClusterName</span></span>
<span data-ttu-id="2a602-119">Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2a602-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="2a602-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a602-120">-DefaultProfile</span></span>
<span data-ttu-id="2a602-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a602-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a602-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a602-122">-InputObject</span></span>
<span data-ttu-id="2a602-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a602-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a602-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2a602-124">-NoWait</span></span>
<span data-ttu-id="2a602-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2a602-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a602-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a602-126">-PassThru</span></span>
<span data-ttu-id="2a602-127">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2a602-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a602-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a602-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a602-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a602-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a602-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a602-130">-SubscriptionId</span></span>
<span data-ttu-id="2a602-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a602-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2a602-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2a602-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2a602-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a602-133">-Confirm</span></span>
<span data-ttu-id="2a602-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a602-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a602-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a602-135">-WhatIf</span></span>
<span data-ttu-id="2a602-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a602-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a602-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a602-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a602-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a602-138">CommonParameters</span></span>
<span data-ttu-id="2a602-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a602-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a602-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a602-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a602-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a602-141">INPUTS</span></span>

### <span data-ttu-id="2a602-142">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="2a602-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="2a602-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a602-143">OUTPUTS</span></span>

### <span data-ttu-id="2a602-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a602-144">System.Boolean</span></span>

## <span data-ttu-id="2a602-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a602-145">NOTES</span></span>

<span data-ttu-id="2a602-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2a602-146">ALIASES</span></span>

<span data-ttu-id="2a602-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a602-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a602-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2a602-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a602-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a602-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a602-150">INPUTobject <IRedisEnterpriseCacheIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2a602-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a602-151">`[ClusterName <String>]`: Nazwa klastra usługi RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2a602-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="2a602-152">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a602-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2a602-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2a602-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a602-154">`[Location <String>]`: Region, w którym znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="2a602-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="2a602-155">`[OperationId <String>]`: Unikatowy identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="2a602-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="2a602-156">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego skojarzonego z zasobem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2a602-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="2a602-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a602-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2a602-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a602-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2a602-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2a602-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2a602-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a602-160">RELATED LINKS</span></span>

