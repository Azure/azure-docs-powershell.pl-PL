---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c658780407454f780ccbd00cb824dd1032f3463d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193154"
---
# <span data-ttu-id="7be74-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7be74-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="7be74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7be74-102">SYNOPSIS</span></span>
<span data-ttu-id="7be74-103">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="7be74-103">Creates a new server.</span></span>

## <span data-ttu-id="7be74-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7be74-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7be74-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7be74-105">DESCRIPTION</span></span>
<span data-ttu-id="7be74-106">Tworzy nowy serwer.</span><span class="sxs-lookup"><span data-stu-id="7be74-106">Creates a new server.</span></span>

## <span data-ttu-id="7be74-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7be74-107">EXAMPLES</span></span>

### <span data-ttu-id="7be74-108">Przykład 1. Tworzenie nowego serwera elastycznego PostgreSql z argumentami</span><span class="sxs-lookup"><span data-stu-id="7be74-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="7be74-109">Przykład 2. Tworzenie nowego serwera elastycznego PostgreSql z ustawieniem domyślnym</span><span class="sxs-lookup"><span data-stu-id="7be74-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="7be74-110">To polecenie cmdlet tworzy elastyczny serwer PostgreSql z domyślnymi wartościami parametrów i zapewnianie obsługi administracyjnej serwera w nowej sieci wirtualnej oraz delegowanie podsieci do serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="7be74-111">Domyślna wartość lokalizacji to Zachód STANÓW Zjednoczonych 2, SKU to Standard_D2s_v3, warstwa SKU to GeneralPurpose, a rozmiar magazynu to 128GiB.</span><span class="sxs-lookup"><span data-stu-id="7be74-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="7be74-112">Jeśli chcesz znaleźć hasło wygenerowane automatycznie dla serwera, użyj programu ConvertFrom-SecureString, aby przekonwertować właściwość "SecuredPassword" na zwykły tekst.</span><span class="sxs-lookup"><span data-stu-id="7be74-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="7be74-113">(Np. $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="7be74-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="7be74-114">Przykład 3. Tworzenie nowego elastycznego serwera PostgreSql z siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="7be74-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7be74-115">To polecenie cmdlet tworzy elastyczny serwer PostgreSql z identyfikatorem vnet lub nazwą sieci vnet podaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7be74-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="7be74-116">Jeśli sieć wirtualna nie istnieje, polecenie cmdlet tworzy sieć.</span><span class="sxs-lookup"><span data-stu-id="7be74-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="7be74-117">Przykład 4. Tworzenie nowego elastycznego serwera PostgreSql z siecią wirtualną i nazwą podsieci</span><span class="sxs-lookup"><span data-stu-id="7be74-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7be74-118">To polecenie cmdlet tworzy elastyczny serwer PostgreSql z nazwą sieci vnet, nazwą podsieci, prefiksem podsieci i prefiksem podsieci.</span><span class="sxs-lookup"><span data-stu-id="7be74-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="7be74-119">Jeśli sieć wirtualna i podsieci wirtualne nie istnieją, polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="7be74-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="7be74-120">Przykład 7. Tworzenie nowego elastycznego serwera PostgreSql z publicznym dostępem do wszystkich ip</span><span class="sxs-lookup"><span data-stu-id="7be74-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="7be74-121">To polecenie cmdlet tworzy elastyczny serwer PostgreSql otwarty dla wszystkich adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7be74-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="7be74-122">Przykład 8. Tworzenie nowego elastycznego serwera PostgreSql z zaporą</span><span class="sxs-lookup"><span data-stu-id="7be74-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7be74-123">To polecenie cmdlet tworzy elastyczny serwer PostgreSql otwarty dla określonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7be74-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="7be74-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7be74-124">PARAMETERS</span></span>

### <span data-ttu-id="7be74-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7be74-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7be74-126">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="7be74-126">The password of the administrator.</span></span>
<span data-ttu-id="7be74-127">Minimalna liczba znaków: 8 i maksymalnie 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="7be74-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="7be74-128">Hasło musi zawierać znaki z trzech z następujących kategorii: angielskie wielkie litery, angielskie małe litery, liczby i znaki niealalnumeryczne.</span><span class="sxs-lookup"><span data-stu-id="7be74-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="7be74-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="7be74-129">-AdministratorUserName</span></span>
<span data-ttu-id="7be74-130">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-130">Administrator username for the server.</span></span>
<span data-ttu-id="7be74-131">Po jej skonfigurowaniu nie będzie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="7be74-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="7be74-132">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7be74-132">-AsJob</span></span>
<span data-ttu-id="7be74-133">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="7be74-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="7be74-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="7be74-134">-BackupRetentionDay</span></span>
<span data-ttu-id="7be74-135">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-135">Backup retention days for the server.</span></span>
<span data-ttu-id="7be74-136">Liczba dni wynosi od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="7be74-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="7be74-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be74-137">-DefaultProfile</span></span>
<span data-ttu-id="7be74-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7be74-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be74-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7be74-139">-Location</span></span>
<span data-ttu-id="7be74-140">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="7be74-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7be74-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7be74-141">-Name</span></span>
<span data-ttu-id="7be74-142">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-142">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be74-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7be74-143">-NoWait</span></span>
<span data-ttu-id="7be74-144">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="7be74-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7be74-145">- PublicAccess</span><span class="sxs-lookup"><span data-stu-id="7be74-145">-PublicAccess</span></span>
<span data-ttu-id="7be74-146">Określa dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="7be74-146">Determines the public access.</span></span>
<span data-ttu-id="7be74-147">Wprowadź jeden lub zakres adresów IP, które mają zostać uwzględnione na liście dozwolonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7be74-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="7be74-148">Zakresy adresów IP muszą być rozdzielone kreskami i nie mogą zawierać spacji.</span><span class="sxs-lookup"><span data-stu-id="7be74-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="7be74-149">Określenie wersji 0.0.0.0 umożliwia dostęp publiczny z dowolnych zasobów wdrożonych na platformie Azure na dostęp do serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="7be74-150">Określenie żadnego adresu IP powoduje ustawienie serwera w trybie dostępu publicznego, ale nie powoduje utworzenia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="7be74-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="7be74-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be74-151">-ResourceGroupName</span></span>
<span data-ttu-id="7be74-152">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="7be74-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7be74-153">- SKU</span><span class="sxs-lookup"><span data-stu-id="7be74-153">-Sku</span></span>
<span data-ttu-id="7be74-154">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="7be74-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="7be74-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7be74-155">-SkuTier</span></span>
<span data-ttu-id="7be74-156">Warstwa obliczeniowa serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-156">Compute tier of the server.</span></span>
<span data-ttu-id="7be74-157">Zaakceptowane wartości: Zbędna seria, OgólnePozyska, Zoptymalizowana pamięć.</span><span class="sxs-lookup"><span data-stu-id="7be74-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="7be74-158">Domyślne: Zamieć na serio.</span><span class="sxs-lookup"><span data-stu-id="7be74-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="7be74-159">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="7be74-159">-StorageInMb</span></span>
<span data-ttu-id="7be74-160">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="7be74-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="7be74-161">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7be74-161">-Subnet</span></span>
<span data-ttu-id="7be74-162">Nazwa lub identyfikator istniejącej podsieci lub nazwa nowej, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="7be74-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="7be74-163">Pamiętaj, że podsieci zostanie delegowana do witryny Microsoft.DBforPostgreSQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="7be74-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="7be74-164">Po delegowaniu tej podsieci nie można używać dla żadnego innego typu zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7be74-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="7be74-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="7be74-165">-SubnetPrefix</span></span>
<span data-ttu-id="7be74-166">Prefiks adresu IP podsieci, który ma być używany podczas tworzenia nowej podsieci w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="7be74-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="7be74-167">Wartość domyślna to 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="7be74-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="7be74-168">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7be74-168">-SubscriptionId</span></span>
<span data-ttu-id="7be74-169">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7be74-169">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7be74-170">— Tag</span><span class="sxs-lookup"><span data-stu-id="7be74-170">-Tag</span></span>
<span data-ttu-id="7be74-171">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="7be74-171">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7be74-172">— Wersja</span><span class="sxs-lookup"><span data-stu-id="7be74-172">-Version</span></span>
<span data-ttu-id="7be74-173">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="7be74-173">Server version.</span></span>

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

### <span data-ttu-id="7be74-174">— Vnet</span><span class="sxs-lookup"><span data-stu-id="7be74-174">-Vnet</span></span>
<span data-ttu-id="7be74-175">Nazwa lub identyfikator istniejącej sieci wirtualnej lub nazwa nowej sieci wirtualnej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="7be74-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="7be74-176">Nazwa musi mieć od 2 do 64 znaków.</span><span class="sxs-lookup"><span data-stu-id="7be74-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="7be74-177">Nazwa musi zaczynać się od litery lub liczby, kończyć się literą, cyfrą lub podkreśleniem i może zawierać tylko litery, cyfry, podkreślenia, kropki lub łączniki.</span><span class="sxs-lookup"><span data-stu-id="7be74-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="7be74-178">- VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="7be74-178">-VnetPrefix</span></span>
<span data-ttu-id="7be74-179">Prefiks adresu IP, który ma być używany podczas tworzenia nowej podsieci w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="7be74-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="7be74-180">Wartość domyślna to 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="7be74-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="7be74-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7be74-181">-Confirm</span></span>
<span data-ttu-id="7be74-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7be74-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be74-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be74-183">-WhatIf</span></span>
<span data-ttu-id="7be74-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7be74-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be74-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7be74-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be74-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be74-186">CommonParameters</span></span>
<span data-ttu-id="7be74-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be74-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be74-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7be74-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be74-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7be74-189">INPUTS</span></span>

## <span data-ttu-id="7be74-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7be74-190">OUTPUTS</span></span>

### <span data-ttu-id="7be74-191">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="7be74-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="7be74-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7be74-192">NOTES</span></span>

<span data-ttu-id="7be74-193">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7be74-193">ALIASES</span></span>

## <span data-ttu-id="7be74-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7be74-194">RELATED LINKS</span></span>

