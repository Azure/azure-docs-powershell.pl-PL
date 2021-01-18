---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500797"
---
# <span data-ttu-id="bb8d0-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="bb8d0-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="bb8d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8d0-103">Tworzy nowy MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bb8d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb8d0-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb8d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb8d0-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8d0-106">Tworzy nowy MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bb8d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb8d0-107">EXAMPLES</span></span>

### <span data-ttu-id="bb8d0-108">Przykład 1. Utwórz nowy MariaDB</span><span class="sxs-lookup"><span data-stu-id="bb8d0-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="bb8d0-109">To polecenie tworzy nowy MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="bb8d0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb8d0-110">PARAMETERS</span></span>

### <span data-ttu-id="bb8d0-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bb8d0-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bb8d0-112">Hasło administratora powinno być poleceniem SecureString.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="bb8d0-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="bb8d0-113">-AdministratorUsername</span></span>
<span data-ttu-id="bb8d0-114">NazwaUżytkownika administratora.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-114">Username of administrator.</span></span>

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

### <span data-ttu-id="bb8d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb8d0-115">-AsJob</span></span>
<span data-ttu-id="bb8d0-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bb8d0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bb8d0-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="bb8d0-117">-BackupRetentionDay</span></span>
<span data-ttu-id="bb8d0-118">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="bb8d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8d0-119">-DefaultProfile</span></span>
<span data-ttu-id="bb8d0-120">Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8d0-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="bb8d0-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="bb8d0-122">Włącz lokalizację geograficzną lub niezbędną dla kopii zapasowych serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="bb8d0-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bb8d0-123">-Location</span></span>
<span data-ttu-id="bb8d0-124">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="bb8d0-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb8d0-125">-Name</span></span>
<span data-ttu-id="bb8d0-126">Nazwa serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="bb8d0-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bb8d0-127">-NoWait</span></span>
<span data-ttu-id="bb8d0-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bb8d0-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb8d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="bb8d0-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="bb8d0-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="bb8d0-131">-Sku</span></span>
<span data-ttu-id="bb8d0-132">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bb8d0-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="bb8d0-133">-SslEnforcement</span></span>
<span data-ttu-id="bb8d0-134">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="bb8d0-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="bb8d0-135">-StorageAutogrow</span></span>
<span data-ttu-id="bb8d0-136">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="bb8d0-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="bb8d0-137">-StorageInMb</span></span>
<span data-ttu-id="bb8d0-138">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="bb8d0-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bb8d0-139">-SubscriptionId</span></span>
<span data-ttu-id="bb8d0-140">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą</span><span class="sxs-lookup"><span data-stu-id="bb8d0-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="bb8d0-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb8d0-141">-Tag</span></span>
<span data-ttu-id="bb8d0-142">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="bb8d0-143">-Version</span><span class="sxs-lookup"><span data-stu-id="bb8d0-143">-Version</span></span>
<span data-ttu-id="bb8d0-144">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-144">Server version.</span></span>

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

### <span data-ttu-id="bb8d0-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb8d0-145">-Confirm</span></span>
<span data-ttu-id="bb8d0-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8d0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8d0-147">-WhatIf</span></span>
<span data-ttu-id="bb8d0-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8d0-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8d0-150">CommonParameters</span></span>
<span data-ttu-id="bb8d0-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8d0-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb8d0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8d0-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb8d0-153">INPUTS</span></span>

## <span data-ttu-id="bb8d0-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb8d0-154">OUTPUTS</span></span>

### <span data-ttu-id="bb8d0-155">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="bb8d0-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="bb8d0-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb8d0-156">NOTES</span></span>

<span data-ttu-id="bb8d0-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bb8d0-157">ALIASES</span></span>

## <span data-ttu-id="bb8d0-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb8d0-158">RELATED LINKS</span></span>

