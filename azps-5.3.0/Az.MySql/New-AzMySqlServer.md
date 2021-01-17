---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490062"
---
# <span data-ttu-id="6936d-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="6936d-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="6936d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6936d-102">SYNOPSIS</span></span>
<span data-ttu-id="6936d-103">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="6936d-103">Creates a new server.</span></span>

## <span data-ttu-id="6936d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6936d-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6936d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6936d-105">DESCRIPTION</span></span>
<span data-ttu-id="6936d-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="6936d-106">Creates a new server.</span></span>

## <span data-ttu-id="6936d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6936d-107">EXAMPLES</span></span>

### <span data-ttu-id="6936d-108">Przykład 1. Tworzenie nowego serwera MySql</span><span class="sxs-lookup"><span data-stu-id="6936d-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6936d-109">Te polecenia cmdlet tworzą nowy serwer MySql.</span><span class="sxs-lookup"><span data-stu-id="6936d-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="6936d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6936d-110">PARAMETERS</span></span>

### <span data-ttu-id="6936d-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6936d-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6936d-112">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="6936d-112">The password of the administrator.</span></span>
<span data-ttu-id="6936d-113">Co najmniej 8 znaków, a maksymalna 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="6936d-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="6936d-114">Hasło musi zawierać znaki z trzech następujących kategorii: wielkie litery angielskie, małe litery angielskie, cyfry i znaki niealfanumeryczne.</span><span class="sxs-lookup"><span data-stu-id="6936d-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="6936d-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="6936d-115">-AdministratorUserName</span></span>
<span data-ttu-id="6936d-116">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-116">Administrator username for the server.</span></span>
<span data-ttu-id="6936d-117">Skonfigurowanej wartości nie można zmienić.</span><span class="sxs-lookup"><span data-stu-id="6936d-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="6936d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6936d-118">-AsJob</span></span>
<span data-ttu-id="6936d-119">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="6936d-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="6936d-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6936d-120">-BackupRetentionDay</span></span>
<span data-ttu-id="6936d-121">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-121">Backup retention days for the server.</span></span>
<span data-ttu-id="6936d-122">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="6936d-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6936d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6936d-123">-DefaultProfile</span></span>
<span data-ttu-id="6936d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6936d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6936d-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="6936d-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="6936d-126">Włącz lokalizację geograficzną lub niezbędną dla kopii zapasowych serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="6936d-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6936d-127">-Location</span></span>
<span data-ttu-id="6936d-128">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="6936d-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6936d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6936d-129">-Name</span></span>
<span data-ttu-id="6936d-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-130">The name of the server.</span></span>

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

### <span data-ttu-id="6936d-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6936d-131">-NoWait</span></span>
<span data-ttu-id="6936d-132">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="6936d-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6936d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6936d-133">-ResourceGroupName</span></span>
<span data-ttu-id="6936d-134">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6936d-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6936d-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="6936d-135">-Sku</span></span>
<span data-ttu-id="6936d-136">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6936d-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6936d-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6936d-137">-SslEnforcement</span></span>
<span data-ttu-id="6936d-138">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="6936d-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="6936d-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6936d-139">-StorageAutogrow</span></span>
<span data-ttu-id="6936d-140">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="6936d-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="6936d-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6936d-141">-StorageInMb</span></span>
<span data-ttu-id="6936d-142">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6936d-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6936d-143">-SubscriptionId</span></span>
<span data-ttu-id="6936d-144">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6936d-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6936d-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="6936d-145">-Tag</span></span>
<span data-ttu-id="6936d-146">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="6936d-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6936d-147">-Version</span><span class="sxs-lookup"><span data-stu-id="6936d-147">-Version</span></span>
<span data-ttu-id="6936d-148">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="6936d-148">Server version.</span></span>

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

### <span data-ttu-id="6936d-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6936d-149">-Confirm</span></span>
<span data-ttu-id="6936d-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6936d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6936d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6936d-151">-WhatIf</span></span>
<span data-ttu-id="6936d-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6936d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6936d-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6936d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6936d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6936d-154">CommonParameters</span></span>
<span data-ttu-id="6936d-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6936d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6936d-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6936d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6936d-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6936d-157">INPUTS</span></span>

## <span data-ttu-id="6936d-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6936d-158">OUTPUTS</span></span>

### <span data-ttu-id="6936d-159">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="6936d-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6936d-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6936d-160">NOTES</span></span>

<span data-ttu-id="6936d-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6936d-161">ALIASES</span></span>

## <span data-ttu-id="6936d-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6936d-162">RELATED LINKS</span></span>

