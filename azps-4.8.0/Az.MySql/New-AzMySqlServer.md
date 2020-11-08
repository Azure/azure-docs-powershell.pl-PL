---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062644"
---
# <span data-ttu-id="9650a-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="9650a-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="9650a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9650a-102">SYNOPSIS</span></span>
<span data-ttu-id="9650a-103">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="9650a-103">Creates a new server.</span></span>

## <span data-ttu-id="9650a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9650a-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9650a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9650a-105">DESCRIPTION</span></span>
<span data-ttu-id="9650a-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="9650a-106">Creates a new server.</span></span>

## <span data-ttu-id="9650a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9650a-107">EXAMPLES</span></span>

### <span data-ttu-id="9650a-108">Przykład 1. Tworzenie nowego serwera MySql</span><span class="sxs-lookup"><span data-stu-id="9650a-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9650a-109">Te polecenia cmdlet tworzą nowy serwer MySql.</span><span class="sxs-lookup"><span data-stu-id="9650a-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="9650a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9650a-110">PARAMETERS</span></span>

### <span data-ttu-id="9650a-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="9650a-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="9650a-112">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="9650a-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9650a-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="9650a-113">-AdministratorUserName</span></span>
<span data-ttu-id="9650a-114">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="9650a-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9650a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9650a-115">-AsJob</span></span>
<span data-ttu-id="9650a-116">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="9650a-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="9650a-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="9650a-117">-BackupRetentionDay</span></span>
<span data-ttu-id="9650a-118">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="9650a-118">Backup retention days for the server.</span></span>
<span data-ttu-id="9650a-119">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="9650a-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="9650a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9650a-120">-DefaultProfile</span></span>
<span data-ttu-id="9650a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9650a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9650a-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="9650a-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="9650a-123">Włącz lokalizację geograficzną lub niezbędną dla kopii zapasowych serwera.</span><span class="sxs-lookup"><span data-stu-id="9650a-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9650a-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9650a-124">-Location</span></span>
<span data-ttu-id="9650a-125">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="9650a-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9650a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9650a-126">-Name</span></span>
<span data-ttu-id="9650a-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9650a-127">The name of the server.</span></span>

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

### <span data-ttu-id="9650a-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9650a-128">-NoWait</span></span>
<span data-ttu-id="9650a-129">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="9650a-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="9650a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9650a-130">-ResourceGroupName</span></span>
<span data-ttu-id="9650a-131">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9650a-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9650a-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="9650a-132">-Sku</span></span>
<span data-ttu-id="9650a-133">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="9650a-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="9650a-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="9650a-134">-SslEnforcement</span></span>
<span data-ttu-id="9650a-135">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="9650a-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="9650a-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="9650a-136">-StorageAutogrow</span></span>
<span data-ttu-id="9650a-137">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="9650a-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="9650a-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="9650a-138">-StorageInMb</span></span>
<span data-ttu-id="9650a-139">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="9650a-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="9650a-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9650a-140">-SubscriptionId</span></span>
<span data-ttu-id="9650a-141">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9650a-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9650a-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9650a-142">-Tag</span></span>
<span data-ttu-id="9650a-143">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="9650a-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="9650a-144">-Version</span><span class="sxs-lookup"><span data-stu-id="9650a-144">-Version</span></span>
<span data-ttu-id="9650a-145">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="9650a-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9650a-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9650a-146">-Confirm</span></span>
<span data-ttu-id="9650a-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9650a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9650a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9650a-148">-WhatIf</span></span>
<span data-ttu-id="9650a-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9650a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9650a-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9650a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9650a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9650a-151">CommonParameters</span></span>
<span data-ttu-id="9650a-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9650a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9650a-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9650a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9650a-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9650a-154">INPUTS</span></span>

## <span data-ttu-id="9650a-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9650a-155">OUTPUTS</span></span>

### <span data-ttu-id="9650a-156">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="9650a-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9650a-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9650a-157">NOTES</span></span>

<span data-ttu-id="9650a-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9650a-158">ALIASES</span></span>

## <span data-ttu-id="9650a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9650a-159">RELATED LINKS</span></span>

