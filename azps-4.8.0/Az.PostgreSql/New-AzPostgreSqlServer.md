---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219324"
---
# <span data-ttu-id="0ff0f-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="0ff0f-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="0ff0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ff0f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff0f-103">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-103">Creates a new server.</span></span>

## <span data-ttu-id="0ff0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ff0f-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ff0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ff0f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff0f-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-106">Creates a new server.</span></span>

## <span data-ttu-id="0ff0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ff0f-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff0f-108">Przykład 1. Tworzenie nowego serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="0ff0f-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0ff0f-109">Te polecenia cmdlet tworzą nowy serwer PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="0ff0f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ff0f-110">PARAMETERS</span></span>

### <span data-ttu-id="0ff0f-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0ff0f-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0ff0f-112">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ff0f-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="0ff0f-113">-AdministratorUserName</span></span>
<span data-ttu-id="0ff0f-114">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ff0f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ff0f-115">-AsJob</span></span>
<span data-ttu-id="0ff0f-116">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="0ff0f-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0ff0f-117">-BackupRetentionDay</span></span>
<span data-ttu-id="0ff0f-118">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-118">Backup retention days for the server.</span></span>
<span data-ttu-id="0ff0f-119">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="0ff0f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff0f-120">-DefaultProfile</span></span>
<span data-ttu-id="0ff0f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff0f-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="0ff0f-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="0ff0f-123">Włącz lokalizację geograficzną lub niezbędną dla kopii zapasowych serwera.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff0f-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0ff0f-124">-Location</span></span>
<span data-ttu-id="0ff0f-125">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ff0f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ff0f-126">-Name</span></span>
<span data-ttu-id="0ff0f-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-127">The name of the server.</span></span>

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

### <span data-ttu-id="0ff0f-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0ff0f-128">-NoWait</span></span>
<span data-ttu-id="0ff0f-129">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0ff0f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff0f-130">-ResourceGroupName</span></span>
<span data-ttu-id="0ff0f-131">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0ff0f-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="0ff0f-132">-Sku</span></span>
<span data-ttu-id="0ff0f-133">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0ff0f-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0ff0f-134">-SslEnforcement</span></span>
<span data-ttu-id="0ff0f-135">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff0f-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="0ff0f-136">-StorageAutogrow</span></span>
<span data-ttu-id="0ff0f-137">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff0f-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0ff0f-138">-StorageInMb</span></span>
<span data-ttu-id="0ff0f-139">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0ff0f-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ff0f-140">-SubscriptionId</span></span>
<span data-ttu-id="0ff0f-141">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0ff0f-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ff0f-142">-Tag</span></span>
<span data-ttu-id="0ff0f-143">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0ff0f-144">-Version</span><span class="sxs-lookup"><span data-stu-id="0ff0f-144">-Version</span></span>
<span data-ttu-id="0ff0f-145">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff0f-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ff0f-146">-Confirm</span></span>
<span data-ttu-id="0ff0f-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff0f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff0f-148">-WhatIf</span></span>
<span data-ttu-id="0ff0f-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff0f-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff0f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff0f-151">CommonParameters</span></span>
<span data-ttu-id="0ff0f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff0f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff0f-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ff0f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff0f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ff0f-154">INPUTS</span></span>

## <span data-ttu-id="0ff0f-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ff0f-155">OUTPUTS</span></span>

### <span data-ttu-id="0ff0f-156">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0ff0f-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0ff0f-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ff0f-157">NOTES</span></span>

<span data-ttu-id="0ff0f-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0ff0f-158">ALIASES</span></span>

## <span data-ttu-id="0ff0f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ff0f-159">RELATED LINKS</span></span>

