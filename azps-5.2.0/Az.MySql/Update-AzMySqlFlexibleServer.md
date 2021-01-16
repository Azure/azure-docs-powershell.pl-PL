---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360227"
---
# <span data-ttu-id="c1e1d-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="c1e1d-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="c1e1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e1d-103">Umożliwia zaktualizowanie istniejącego serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="c1e1d-104">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c1e1d-105">Zamiast tego użyj Update-AzMySqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c1e1d-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1e1d-106">SYNTAX</span></span>

### <span data-ttu-id="c1e1d-107">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1e1d-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1e1d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c1e1d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1e1d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c1e1d-109">DESCRIPTION</span></span>
<span data-ttu-id="c1e1d-110">Umożliwia zaktualizowanie istniejącego serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="c1e1d-111">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c1e1d-112">Zamiast tego użyj Update-AzMySqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c1e1d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1e1d-113">EXAMPLES</span></span>

### <span data-ttu-id="c1e1d-114">Przykład 1: aktualizowanie serwera MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="c1e1d-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="c1e1d-115">To polecenie cmdlet aktualizuje serwer MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="c1e1d-116">Przykład 2: aktualizowanie serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c1e1d-117">To polecenie cmdlet aktualizuje serwer MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="c1e1d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1e1d-118">PARAMETERS</span></span>

### <span data-ttu-id="c1e1d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c1e1d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c1e1d-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1e1d-121">-AsJob</span></span>
<span data-ttu-id="c1e1d-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="c1e1d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c1e1d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="c1e1d-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="c1e1d-125">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e1d-126">-DefaultProfile</span></span>
<span data-ttu-id="c1e1d-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1e1d-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="c1e1d-128">-HaEnabled</span></span>
<span data-ttu-id="c1e1d-129">Włączanie lub wyłączanie funkcji wysokiej dostępności.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1e1d-130">-InputObject</span></span>
<span data-ttu-id="c1e1d-131">Parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-131">Identity Parameter.</span></span>
<span data-ttu-id="c1e1d-132">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1e1d-133">-Name</span></span>
<span data-ttu-id="c1e1d-134">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-134">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c1e1d-135">-NoWait</span></span>
<span data-ttu-id="c1e1d-136">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c1e1d-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="c1e1d-137">-ReplicationRole</span></span>
<span data-ttu-id="c1e1d-138">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="c1e1d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e1d-139">-ResourceGroupName</span></span>
<span data-ttu-id="c1e1d-140">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c1e1d-141">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1e1d-142">-Sku</span></span>
<span data-ttu-id="c1e1d-143">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c1e1d-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c1e1d-144">-SkuTier</span></span>
<span data-ttu-id="c1e1d-145">Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-145">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c1e1d-146">-SslEnforcement</span></span>
<span data-ttu-id="c1e1d-147">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-147">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c1e1d-148">-StorageAutogrow</span></span>
<span data-ttu-id="c1e1d-149">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-149">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c1e1d-150">-StorageInMb</span></span>
<span data-ttu-id="c1e1d-151">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-151">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c1e1d-152">-SubscriptionId</span></span>
<span data-ttu-id="c1e1d-153">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-153">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1e1d-154">-Tag</span></span>
<span data-ttu-id="c1e1d-155">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-155">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1d-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1e1d-156">-Confirm</span></span>
<span data-ttu-id="c1e1d-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e1d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e1d-158">-WhatIf</span></span>
<span data-ttu-id="c1e1d-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1e1d-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1e1d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e1d-161">CommonParameters</span></span>
<span data-ttu-id="c1e1d-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e1d-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1e1d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e1d-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1e1d-164">INPUTS</span></span>

### <span data-ttu-id="c1e1d-165">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c1e1d-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c1e1d-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1e1d-166">OUTPUTS</span></span>

### <span data-ttu-id="c1e1d-167">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c1e1d-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="c1e1d-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1e1d-168">NOTES</span></span>

<span data-ttu-id="c1e1d-169">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c1e1d-169">ALIASES</span></span>

<span data-ttu-id="c1e1d-170">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1e1d-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1e1d-171">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1e1d-172">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1e1d-173">INPUTobject <IMySqlIdentity> : parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c1e1d-174">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c1e1d-175">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c1e1d-176">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c1e1d-177">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c1e1d-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1e1d-178">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c1e1d-179">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c1e1d-180">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c1e1d-181">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="c1e1d-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c1e1d-183">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c1e1d-184">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c1e1d-185">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c1e1d-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1e1d-186">RELATED LINKS</span></span>

