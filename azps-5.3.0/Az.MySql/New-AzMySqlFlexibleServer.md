---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503285"
---
# <span data-ttu-id="b4320-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b4320-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="b4320-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4320-102">SYNOPSIS</span></span>
<span data-ttu-id="b4320-103">Tworzy nowy serwer elastyczny MySQL</span><span class="sxs-lookup"><span data-stu-id="b4320-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="b4320-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4320-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4320-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4320-105">DESCRIPTION</span></span>
<span data-ttu-id="b4320-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="b4320-106">Creates a new server.</span></span>

## <span data-ttu-id="b4320-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4320-107">EXAMPLES</span></span>

### <span data-ttu-id="b4320-108">Przykład 1. Tworzenie nowego serwera elastycznego MySql</span><span class="sxs-lookup"><span data-stu-id="b4320-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="b4320-109">Przykład 2: Tworzenie nowego serwera elastycznego MySql z ustawieniem domyślnym</span><span class="sxs-lookup"><span data-stu-id="b4320-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="b4320-110">Utwórz serwer MySql z wartościami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="b4320-110">Create MySql server with default values.</span></span>
<span data-ttu-id="b4320-111">Domyślne wartości lokalizacji to zachodni stan 2, jednostka SKU to Standard_B1ms, warstwa SKU jest rozbudowana, a rozmiar magazynu to 10GiB.</span><span class="sxs-lookup"><span data-stu-id="b4320-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="b4320-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4320-112">PARAMETERS</span></span>

### <span data-ttu-id="b4320-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b4320-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b4320-114">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="b4320-114">The password of the administrator.</span></span>
<span data-ttu-id="b4320-115">Co najmniej 8 znaków, a maksymalna 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="b4320-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b4320-116">Hasło musi zawierać znaki z trzech następujących kategorii: wielkie litery angielskie, małe litery angielskie, cyfry i znaki niealfanumeryczne.</span><span class="sxs-lookup"><span data-stu-id="b4320-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b4320-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b4320-117">-AdministratorUserName</span></span>
<span data-ttu-id="b4320-118">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-118">Administrator username for the server.</span></span>
<span data-ttu-id="b4320-119">Skonfigurowanej wartości nie można zmienić.</span><span class="sxs-lookup"><span data-stu-id="b4320-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b4320-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4320-120">-AsJob</span></span>
<span data-ttu-id="b4320-121">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="b4320-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="b4320-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b4320-122">-BackupRetentionDay</span></span>
<span data-ttu-id="b4320-123">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-123">Backup retention days for the server.</span></span>
<span data-ttu-id="b4320-124">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="b4320-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b4320-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4320-125">-DefaultProfile</span></span>
<span data-ttu-id="b4320-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4320-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4320-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4320-127">-Location</span></span>
<span data-ttu-id="b4320-128">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="b4320-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b4320-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4320-129">-Name</span></span>
<span data-ttu-id="b4320-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-130">The name of the server.</span></span>

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

### <span data-ttu-id="b4320-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b4320-131">-NoWait</span></span>
<span data-ttu-id="b4320-132">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="b4320-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b4320-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4320-133">-ResourceGroupName</span></span>
<span data-ttu-id="b4320-134">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b4320-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b4320-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="b4320-135">-Sku</span></span>
<span data-ttu-id="b4320-136">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="b4320-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="b4320-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b4320-137">-SkuTier</span></span>
<span data-ttu-id="b4320-138">Warstwa obliczeniowa serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-138">Compute tier of the server.</span></span>
<span data-ttu-id="b4320-139">Akceptowane wartości: z serii, GeneralPurpose, zoptymalizowana pamięć.</span><span class="sxs-lookup"><span data-stu-id="b4320-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="b4320-140">Wartość domyślna: do zaszeregowania.</span><span class="sxs-lookup"><span data-stu-id="b4320-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="b4320-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b4320-141">-StorageInMb</span></span>
<span data-ttu-id="b4320-142">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b4320-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b4320-143">-SubscriptionId</span></span>
<span data-ttu-id="b4320-144">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4320-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b4320-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4320-145">-Tag</span></span>
<span data-ttu-id="b4320-146">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="b4320-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b4320-147">-Version</span><span class="sxs-lookup"><span data-stu-id="b4320-147">-Version</span></span>
<span data-ttu-id="b4320-148">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="b4320-148">Server version.</span></span>

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

### <span data-ttu-id="b4320-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4320-149">-Confirm</span></span>
<span data-ttu-id="b4320-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4320-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4320-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4320-151">-WhatIf</span></span>
<span data-ttu-id="b4320-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4320-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4320-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4320-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4320-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4320-154">CommonParameters</span></span>
<span data-ttu-id="b4320-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4320-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4320-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4320-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4320-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4320-157">INPUTS</span></span>

## <span data-ttu-id="b4320-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4320-158">OUTPUTS</span></span>

### <span data-ttu-id="b4320-159">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b4320-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="b4320-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4320-160">NOTES</span></span>

<span data-ttu-id="b4320-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b4320-161">ALIASES</span></span>

## <span data-ttu-id="b4320-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4320-162">RELATED LINKS</span></span>

