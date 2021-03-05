---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: ccd05d8c0a7678b16831659fb0ca119adf94ddae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961841"
---
# <span data-ttu-id="8ac17-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="8ac17-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="8ac17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac17-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac17-103">Tworzy nową plik MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8ac17-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="8ac17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ac17-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ac17-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ac17-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac17-106">Tworzy nową plik MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8ac17-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="8ac17-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ac17-107">EXAMPLES</span></span>

### <span data-ttu-id="8ac17-108">Przykład 1. Tworzenie nowej bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="8ac17-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="8ac17-109">To polecenie powoduje utworzenie nowej bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8ac17-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="8ac17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ac17-110">PARAMETERS</span></span>

### <span data-ttu-id="8ac17-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8ac17-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8ac17-112">Hasło administratora powinno mieć hasłem SecureString.</span><span class="sxs-lookup"><span data-stu-id="8ac17-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="8ac17-113">-AdministratorUsername</span></span>
<span data-ttu-id="8ac17-114">Nazwa użytkownika administratora.</span><span class="sxs-lookup"><span data-stu-id="8ac17-114">Username of administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8ac17-115">-AsJob</span></span>
<span data-ttu-id="8ac17-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8ac17-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8ac17-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8ac17-117">-BackupRetentionDay</span></span>
<span data-ttu-id="8ac17-118">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8ac17-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="8ac17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac17-119">-DefaultProfile</span></span>
<span data-ttu-id="8ac17-120">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac17-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac17-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="8ac17-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="8ac17-122">Włączanie nadmiarowej lokalizacji geograficznej dla kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8ac17-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ac17-123">-Location</span></span>
<span data-ttu-id="8ac17-124">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8ac17-124">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ac17-125">-Name</span></span>
<span data-ttu-id="8ac17-126">Nazwa serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8ac17-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ac17-127">-NoWait</span></span>
<span data-ttu-id="8ac17-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8ac17-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8ac17-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac17-129">-ResourceGroupName</span></span>
<span data-ttu-id="8ac17-130">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="8ac17-130">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-131">- SKU</span><span class="sxs-lookup"><span data-stu-id="8ac17-131">-Sku</span></span>
<span data-ttu-id="8ac17-132">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8ac17-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-133">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8ac17-133">-SslEnforcement</span></span>
<span data-ttu-id="8ac17-134">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="8ac17-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-135">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8ac17-135">-StorageAutogrow</span></span>
<span data-ttu-id="8ac17-136">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8ac17-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-137">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8ac17-137">-StorageInMb</span></span>
<span data-ttu-id="8ac17-138">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8ac17-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8ac17-139">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ac17-139">-SubscriptionId</span></span>
<span data-ttu-id="8ac17-140">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi</span><span class="sxs-lookup"><span data-stu-id="8ac17-140">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-141">— Tag</span><span class="sxs-lookup"><span data-stu-id="8ac17-141">-Tag</span></span>
<span data-ttu-id="8ac17-142">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8ac17-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8ac17-143">— Wersja</span><span class="sxs-lookup"><span data-stu-id="8ac17-143">-Version</span></span>
<span data-ttu-id="8ac17-144">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="8ac17-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ac17-145">-Confirm</span></span>
<span data-ttu-id="8ac17-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ac17-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac17-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac17-147">-WhatIf</span></span>
<span data-ttu-id="8ac17-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac17-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ac17-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8ac17-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac17-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac17-150">CommonParameters</span></span>
<span data-ttu-id="8ac17-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac17-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac17-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ac17-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac17-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac17-153">INPUTS</span></span>

## <span data-ttu-id="8ac17-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac17-154">OUTPUTS</span></span>

### <span data-ttu-id="8ac17-155">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="8ac17-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8ac17-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ac17-156">NOTES</span></span>

<span data-ttu-id="8ac17-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8ac17-157">ALIASES</span></span>

## <span data-ttu-id="8ac17-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac17-158">RELATED LINKS</span></span>

