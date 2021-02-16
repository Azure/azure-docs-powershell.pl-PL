---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 37e8896389931f6909d783cbb07a694ed6186fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241187"
---
# <span data-ttu-id="8bd5b-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8bd5b-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="8bd5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd5b-103">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-103">Creates a new server.</span></span>

## <span data-ttu-id="8bd5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bd5b-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8bd5b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd5b-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-106">Creates a new server.</span></span>

## <span data-ttu-id="8bd5b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bd5b-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd5b-108">Przykład 1. Tworzenie nowego serwera MySql</span><span class="sxs-lookup"><span data-stu-id="8bd5b-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8bd5b-109">Te polecenia cmdlet tworzą nowy serwer MySql.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="8bd5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bd5b-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd5b-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8bd5b-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8bd5b-112">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-112">The password of the administrator.</span></span>
<span data-ttu-id="8bd5b-113">Minimalna liczba znaków: 8 i maksymalnie 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="8bd5b-114">Hasło musi zawierać znaki z trzech z następujących kategorii: angielskie wielkie litery, angielskie małe litery, liczby i znaki niealalnumeryczne.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="8bd5b-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="8bd5b-115">-AdministratorUserName</span></span>
<span data-ttu-id="8bd5b-116">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-116">Administrator username for the server.</span></span>
<span data-ttu-id="8bd5b-117">Po jej skonfigurowaniu nie będzie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="8bd5b-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8bd5b-118">-AsJob</span></span>
<span data-ttu-id="8bd5b-119">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="8bd5b-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8bd5b-120">-BackupRetentionDay</span></span>
<span data-ttu-id="8bd5b-121">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-121">Backup retention days for the server.</span></span>
<span data-ttu-id="8bd5b-122">Liczba dni wynosi między 7 a 35.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8bd5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd5b-123">-DefaultProfile</span></span>
<span data-ttu-id="8bd5b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd5b-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="8bd5b-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="8bd5b-126">Włączanie nadmiarowej lokalizacji geograficznej dla kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="8bd5b-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8bd5b-127">-Location</span></span>
<span data-ttu-id="8bd5b-128">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8bd5b-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8bd5b-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="8bd5b-130">Ustaw minimalną wersję protokołu TLS dla połączeń z serwerem, gdy jest włączony protokół SSL.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="8bd5b-131">Wartości domyślne to TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd5b-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8bd5b-132">-Name</span></span>
<span data-ttu-id="8bd5b-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-133">The name of the server.</span></span>

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

### <span data-ttu-id="8bd5b-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8bd5b-134">-NoWait</span></span>
<span data-ttu-id="8bd5b-135">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8bd5b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd5b-136">-ResourceGroupName</span></span>
<span data-ttu-id="8bd5b-137">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8bd5b-138">- SKU</span><span class="sxs-lookup"><span data-stu-id="8bd5b-138">-Sku</span></span>
<span data-ttu-id="8bd5b-139">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8bd5b-140">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8bd5b-140">-SslEnforcement</span></span>
<span data-ttu-id="8bd5b-141">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-141">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="8bd5b-142">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8bd5b-142">-StorageAutogrow</span></span>
<span data-ttu-id="8bd5b-143">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-143">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="8bd5b-144">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8bd5b-144">-StorageInMb</span></span>
<span data-ttu-id="8bd5b-145">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8bd5b-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bd5b-146">-SubscriptionId</span></span>
<span data-ttu-id="8bd5b-147">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8bd5b-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="8bd5b-148">-Tag</span></span>
<span data-ttu-id="8bd5b-149">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8bd5b-150">— Wersja</span><span class="sxs-lookup"><span data-stu-id="8bd5b-150">-Version</span></span>
<span data-ttu-id="8bd5b-151">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-151">Server version.</span></span>

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

### <span data-ttu-id="8bd5b-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bd5b-152">-Confirm</span></span>
<span data-ttu-id="8bd5b-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd5b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd5b-154">-WhatIf</span></span>
<span data-ttu-id="8bd5b-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd5b-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd5b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd5b-157">CommonParameters</span></span>
<span data-ttu-id="8bd5b-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd5b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd5b-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bd5b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd5b-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bd5b-160">INPUTS</span></span>

## <span data-ttu-id="8bd5b-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bd5b-161">OUTPUTS</span></span>

### <span data-ttu-id="8bd5b-162">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="8bd5b-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8bd5b-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bd5b-163">NOTES</span></span>

<span data-ttu-id="8bd5b-164">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8bd5b-164">ALIASES</span></span>

## <span data-ttu-id="8bd5b-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bd5b-165">RELATED LINKS</span></span>

