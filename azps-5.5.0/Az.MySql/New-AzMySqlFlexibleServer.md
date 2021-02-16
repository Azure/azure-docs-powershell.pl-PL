---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: c544ce2ea5f02d5c0b3b7aee41e19992a0dc356d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192114"
---
# <span data-ttu-id="170b6-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="170b6-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="170b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170b6-102">SYNOPSIS</span></span>
<span data-ttu-id="170b6-103">Tworzy nowy elastyczny serwer MySQL.</span><span class="sxs-lookup"><span data-stu-id="170b6-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="170b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="170b6-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="170b6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="170b6-105">DESCRIPTION</span></span>
<span data-ttu-id="170b6-106">Tworzy nowy elastyczny serwer MySQL.</span><span class="sxs-lookup"><span data-stu-id="170b6-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="170b6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="170b6-107">EXAMPLES</span></span>

### <span data-ttu-id="170b6-108">Przykład 1. Tworzenie nowego elastycznego serwera MySql z argumentami</span><span class="sxs-lookup"><span data-stu-id="170b6-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="170b6-109">Przykład 2. Tworzenie nowego serwera elastycznego MySql z ustawieniem domyślnym</span><span class="sxs-lookup"><span data-stu-id="170b6-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="170b6-110">To polecenie cmdlet tworzy elastyczny serwer MySql z domyślnymi wartościami parametrów i zapewnianie obsługi administracyjnej serwera w nowej sieci wirtualnej oraz delegowanie podsieci do serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="170b6-111">Domyślne wartości lokalizacji to Zachód STANÓW Zjednoczonych 2, SKU to Standard_B1ms, warstwa SKU może być dyskowa, a rozmiar magazynu to 10GiB.</span><span class="sxs-lookup"><span data-stu-id="170b6-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="170b6-112">Jeśli chcesz znaleźć hasło wygenerowane automatycznie dla serwera, użyj programu ConvertFrom-SecureString, aby przekonwertować właściwość "SecuredPassword" na zwykły tekst.</span><span class="sxs-lookup"><span data-stu-id="170b6-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="170b6-113">(Np. $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="170b6-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="170b6-114">Przykład 3. Tworzenie nowego elastycznego serwera MySql z siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="170b6-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="170b6-115">To polecenie cmdlet tworzy elastyczny serwer MySql z identyfikatorem vnet lub nazwą sieci vnet podaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="170b6-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="170b6-116">Jeśli sieć wirtualna nie istnieje, polecenie cmdlet tworzy sieć.</span><span class="sxs-lookup"><span data-stu-id="170b6-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="170b6-117">Przykład 4. Tworzenie nowego elastycznego serwera MySql z siecią wirtualną i nazwą podsieci</span><span class="sxs-lookup"><span data-stu-id="170b6-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="170b6-118">To polecenie cmdlet tworzy elastyczny serwer MySql z nazwą sieci vnet, nazwą podsieci, prefiksem podsieci i prefiksem podsieci.</span><span class="sxs-lookup"><span data-stu-id="170b6-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="170b6-119">Jeśli sieć wirtualna i podsieci wirtualne nie istnieją, polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="170b6-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="170b6-120">Przykład 7. Tworzenie nowego elastycznego serwera MySql z publicznym dostępem do wszystkich ip</span><span class="sxs-lookup"><span data-stu-id="170b6-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="170b6-121">To polecenie cmdlet tworzy elastyczny serwer MySql otwarty dla wszystkich adresów IP.</span><span class="sxs-lookup"><span data-stu-id="170b6-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="170b6-122">Przykład 8. Tworzenie nowego elastycznego serwera MySql z zaporą</span><span class="sxs-lookup"><span data-stu-id="170b6-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="170b6-123">To polecenie cmdlet tworzy elastyczny serwer MySql otwarty dla określonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="170b6-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="170b6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="170b6-124">PARAMETERS</span></span>

### <span data-ttu-id="170b6-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="170b6-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="170b6-126">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="170b6-126">The password of the administrator.</span></span>
<span data-ttu-id="170b6-127">Minimalna liczba znaków: 8 i maksymalnie 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="170b6-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="170b6-128">Hasło musi zawierać znaki z trzech z następujących kategorii: angielskie wielkie litery, angielskie małe litery, liczby i znaki niealalnumeryczne.</span><span class="sxs-lookup"><span data-stu-id="170b6-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="170b6-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="170b6-129">-AdministratorUserName</span></span>
<span data-ttu-id="170b6-130">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-130">Administrator username for the server.</span></span>
<span data-ttu-id="170b6-131">Po jej skonfigurowaniu nie będzie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="170b6-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="170b6-132">— AsJob</span><span class="sxs-lookup"><span data-stu-id="170b6-132">-AsJob</span></span>
<span data-ttu-id="170b6-133">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="170b6-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="170b6-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="170b6-134">-BackupRetentionDay</span></span>
<span data-ttu-id="170b6-135">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-135">Backup retention days for the server.</span></span>
<span data-ttu-id="170b6-136">Liczba dni wynosi od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="170b6-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="170b6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170b6-137">-DefaultProfile</span></span>
<span data-ttu-id="170b6-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="170b6-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="170b6-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="170b6-139">-HighAvailability</span></span>
<span data-ttu-id="170b6-140">Włączanie lub wyłączanie funkcji wysokiej dostępności.</span><span class="sxs-lookup"><span data-stu-id="170b6-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="170b6-141">Wartość domyślna to Disabled (Wyłączone).</span><span class="sxs-lookup"><span data-stu-id="170b6-141">Default value is Disabled.</span></span>
<span data-ttu-id="170b6-142">Domyślne: Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="170b6-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170b6-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="170b6-143">-Location</span></span>
<span data-ttu-id="170b6-144">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="170b6-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="170b6-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="170b6-145">-Name</span></span>
<span data-ttu-id="170b6-146">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-146">The name of the server.</span></span>

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

### <span data-ttu-id="170b6-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="170b6-147">-NoWait</span></span>
<span data-ttu-id="170b6-148">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="170b6-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="170b6-149">- PublicAccess</span><span class="sxs-lookup"><span data-stu-id="170b6-149">-PublicAccess</span></span>
<span data-ttu-id="170b6-150">Określa dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="170b6-150">Determines the public access.</span></span>
<span data-ttu-id="170b6-151">Wprowadź jeden lub zakres adresów IP, które mają zostać uwzględnione na liście dozwolonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="170b6-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="170b6-152">Zakresy adresów IP muszą być rozdzielone kreskami i nie mogą zawierać spacji.</span><span class="sxs-lookup"><span data-stu-id="170b6-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="170b6-153">Określenie wersji 0.0.0.0 umożliwia dostęp publiczny z dowolnych zasobów wdrożonych na platformie Azure na dostęp do serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="170b6-154">Określenie żadnego adresu IP powoduje ustawienie serwera w trybie dostępu publicznego, ale nie powoduje utworzenia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="170b6-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="170b6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170b6-155">-ResourceGroupName</span></span>
<span data-ttu-id="170b6-156">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="170b6-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="170b6-157">- SKU</span><span class="sxs-lookup"><span data-stu-id="170b6-157">-Sku</span></span>
<span data-ttu-id="170b6-158">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="170b6-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="170b6-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="170b6-159">-SkuTier</span></span>
<span data-ttu-id="170b6-160">Warstwa obliczeniowa serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-160">Compute tier of the server.</span></span>
<span data-ttu-id="170b6-161">Zaakceptowane wartości: Zbędna seria, OgólnePozyska, Zoptymalizowana pamięć.</span><span class="sxs-lookup"><span data-stu-id="170b6-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="170b6-162">Domyślne: Zamieć na serio.</span><span class="sxs-lookup"><span data-stu-id="170b6-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="170b6-163">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="170b6-163">-StorageInMb</span></span>
<span data-ttu-id="170b6-164">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="170b6-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="170b6-165">-Subnet</span><span class="sxs-lookup"><span data-stu-id="170b6-165">-Subnet</span></span>
<span data-ttu-id="170b6-166">Nazwa lub identyfikator istniejącej podsieci lub nazwa nowej, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="170b6-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="170b6-167">Pamiętaj, że podsieci zostanie delegowana na serwery Microsoft.DBforMySQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="170b6-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="170b6-168">Po delegowaniu tej podsieci nie można używać dla żadnego innego typu zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="170b6-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="170b6-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="170b6-169">-SubnetPrefix</span></span>
<span data-ttu-id="170b6-170">Prefiks adresu IP podsieci, który ma być używany podczas tworzenia nowej podsieci w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="170b6-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="170b6-171">Wartość domyślna to 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="170b6-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="170b6-172">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="170b6-172">-SubscriptionId</span></span>
<span data-ttu-id="170b6-173">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="170b6-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="170b6-174">— Tag</span><span class="sxs-lookup"><span data-stu-id="170b6-174">-Tag</span></span>
<span data-ttu-id="170b6-175">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="170b6-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="170b6-176">— Wersja</span><span class="sxs-lookup"><span data-stu-id="170b6-176">-Version</span></span>
<span data-ttu-id="170b6-177">Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="170b6-177">Server version.</span></span>

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

### <span data-ttu-id="170b6-178">— Vnet</span><span class="sxs-lookup"><span data-stu-id="170b6-178">-Vnet</span></span>
<span data-ttu-id="170b6-179">Nazwa lub identyfikator istniejącej sieci wirtualnej lub nazwa nowej sieci wirtualnej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="170b6-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="170b6-180">Nazwa musi mieć od 2 do 64 znaków.</span><span class="sxs-lookup"><span data-stu-id="170b6-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="170b6-181">Nazwa musi zaczynać się od litery lub liczby, kończyć się literą, cyfrą lub podkreśleniem i może zawierać tylko litery, cyfry, podkreślenia, kropki lub łączniki.</span><span class="sxs-lookup"><span data-stu-id="170b6-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="170b6-182">- VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="170b6-182">-VnetPrefix</span></span>
<span data-ttu-id="170b6-183">Prefiks adresu IP, który ma być używany podczas tworzenia nowej podsieci w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="170b6-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="170b6-184">Wartość domyślna to 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="170b6-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="170b6-185">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="170b6-185">-Confirm</span></span>
<span data-ttu-id="170b6-186">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="170b6-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170b6-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170b6-187">-WhatIf</span></span>
<span data-ttu-id="170b6-188">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="170b6-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="170b6-189">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="170b6-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170b6-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170b6-190">CommonParameters</span></span>
<span data-ttu-id="170b6-191">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170b6-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170b6-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="170b6-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170b6-193">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170b6-193">INPUTS</span></span>

## <span data-ttu-id="170b6-194">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170b6-194">OUTPUTS</span></span>

### <span data-ttu-id="170b6-195">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="170b6-195">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="170b6-196">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="170b6-196">NOTES</span></span>

<span data-ttu-id="170b6-197">ALIASY</span><span class="sxs-lookup"><span data-stu-id="170b6-197">ALIASES</span></span>

## <span data-ttu-id="170b6-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="170b6-198">RELATED LINKS</span></span>

