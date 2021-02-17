---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197707"
---
# <span data-ttu-id="75cf1-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="75cf1-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="75cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="75cf1-103">Tworzy wystąpienie zarządzane usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="75cf1-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="75cf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75cf1-104">SYNTAX</span></span>

### <span data-ttu-id="75cf1-105">NewByEditionAndComputeGenerParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="75cf1-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75cf1-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75cf1-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75cf1-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75cf1-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75cf1-108">NewBySkuNameParameterSetParameters</span><span class="sxs-lookup"><span data-stu-id="75cf1-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cf1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="75cf1-109">DESCRIPTION</span></span>
<span data-ttu-id="75cf1-110">Polecenie **cmdlet New-AzSqlInstance** tworzy wystąpienie zarządzane przez usługę Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="75cf1-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="75cf1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75cf1-111">EXAMPLES</span></span>

### <span data-ttu-id="75cf1-112">Przykład 1. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="75cf1-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="75cf1-113">To polecenie tworzy nowe wystąpienie przy użyciu parametru SKUName.</span><span class="sxs-lookup"><span data-stu-id="75cf1-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="75cf1-114">Przykład 2. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="75cf1-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="75cf1-115">To polecenie tworzy nowe wystąpienie przy użyciu parametrów Edition i Compute Zwyrodnienie.</span><span class="sxs-lookup"><span data-stu-id="75cf1-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="75cf1-116">Przykład 3. Tworzenie nowego wystąpienia w puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="75cf1-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="75cf1-117">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="75cf1-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="75cf1-118">Przykład 4. Tworzenie nowego wystąpienia w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="75cf1-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="75cf1-119">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="75cf1-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="75cf1-120">Przykład 5. Tworzenie nowego wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="75cf1-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="75cf1-121">To polecenie tworzy nowe wystąpienie w puli wystąpień z wystąpieniem nazwPool0</span><span class="sxs-lookup"><span data-stu-id="75cf1-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="75cf1-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cf1-122">PARAMETERS</span></span>

### <span data-ttu-id="75cf1-123">- AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="75cf1-123">-AdministratorCredential</span></span>
<span data-ttu-id="75cf1-124">Poświadczenia uwierzytelniania SQL wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="75cf1-125">-AsJob</span></span>
<span data-ttu-id="75cf1-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="75cf1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75cf1-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="75cf1-127">-AssignIdentity</span></span>
<span data-ttu-id="75cf1-128">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zarządzanego wystąpienia do użycia z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="75cf1-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="75cf1-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="75cf1-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="75cf1-130">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla wystąpienia zarządzanego platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="75cf1-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="75cf1-131">Dostępne opcje: Lokalny, Strefowy i Geolokalizacji</span><span class="sxs-lookup"><span data-stu-id="75cf1-131">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-132">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="75cf1-132">-Collation</span></span>
<span data-ttu-id="75cf1-133">Sortowanie wystąpienia zarządzanego przez język Azure SQL do użycia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="75cf1-134">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="75cf1-134">-ComputeGeneration</span></span>
<span data-ttu-id="75cf1-135">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-135">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cf1-136">-DefaultProfile</span></span>
<span data-ttu-id="75cf1-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75cf1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="75cf1-138">-DnsZonePartner</span></span>
<span data-ttu-id="75cf1-139">Identyfikator zasobu zarządzanego serwera partnerskiego, który dziedziczy właściwość DnsZone po utworzeniu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="75cf1-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="75cf1-140">— wersja</span><span class="sxs-lookup"><span data-stu-id="75cf1-140">-Edition</span></span>
<span data-ttu-id="75cf1-141">Wersja tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-141">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-142">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="75cf1-142">-Force</span></span>
<span data-ttu-id="75cf1-143">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="75cf1-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="75cf1-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="75cf1-144">-InstancePool</span></span>
<span data-ttu-id="75cf1-145">Obiekt nadrzędny puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="75cf1-145">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="75cf1-146">-InstancePoolName</span></span>
<span data-ttu-id="75cf1-147">Pula wystąpień, w którym należy umieścić to wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="75cf1-147">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="75cf1-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="75cf1-149">Identyfikator zasobu puli wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-149">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="75cf1-150">-LicenseType</span></span>
<span data-ttu-id="75cf1-151">Określenie typu licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="75cf1-151">Determines which License Type to use.</span></span> <span data-ttu-id="75cf1-152">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="75cf1-152">Possible values are:</span></span>
- <span data-ttu-id="75cf1-153">Cena Bazowa — zastosowano rabat w ramach korzyści hybrydowej platformy Azure (AHB) dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75cf1-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="75cf1-154">Cena usługi zarządzanego wystąpienia zostanie zdyskoowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75cf1-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="75cf1-155">Cena rabatu z rabatem na usługę Azure Hybrid Benefit (AHB) dla istniejących właścicieli licencji programu SQL Server nie jest stosowana.</span><span class="sxs-lookup"><span data-stu-id="75cf1-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="75cf1-156">Cena usługi zarządzanego wystąpienia będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75cf1-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="75cf1-157">-Location</span></span>
<span data-ttu-id="75cf1-158">Lokalizacja, w której ma być tworzyć wystąpienie</span><span class="sxs-lookup"><span data-stu-id="75cf1-158">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-159">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="75cf1-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="75cf1-160">Identyfikator konfiguracji konserwacji dla wystąpienia zarządzanego platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="75cf1-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="75cf1-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="75cf1-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="75cf1-162">Minimalna wersja TLS wymuszana dla wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="75cf1-162">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-163">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75cf1-163">-Name</span></span>
<span data-ttu-id="75cf1-164">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75cf1-164">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="75cf1-165">-ProxyOverride</span></span>
<span data-ttu-id="75cf1-166">Typ połączenia używany do łączenia się z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="75cf1-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="75cf1-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="75cf1-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="75cf1-168">Czy dla wystąpienia jest włączony publiczny punkt końcowy danych.</span><span class="sxs-lookup"><span data-stu-id="75cf1-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="75cf1-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cf1-169">-ResourceGroupName</span></span>
<span data-ttu-id="75cf1-170">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75cf1-170">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-171">-SKUName</span><span class="sxs-lookup"><span data-stu-id="75cf1-171">-SkuName</span></span>
<span data-ttu-id="75cf1-172">Nazwa SKU wystąpienia, na przykład "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="75cf1-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-173">- StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="75cf1-173">-StorageSizeInGB</span></span>
<span data-ttu-id="75cf1-174">Określa, ile miejsca do magazynowania należy skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="75cf1-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="75cf1-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="75cf1-175">-SubnetId</span></span>
<span data-ttu-id="75cf1-176">Identyfikator podsieci do użycia podczas tworzenia wystąpień</span><span class="sxs-lookup"><span data-stu-id="75cf1-176">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-177">— Tag</span><span class="sxs-lookup"><span data-stu-id="75cf1-177">-Tag</span></span>
<span data-ttu-id="75cf1-178">Tagi do skojarzenia z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="75cf1-178">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-179">- TimezoneId</span><span class="sxs-lookup"><span data-stu-id="75cf1-179">-TimezoneId</span></span>
<span data-ttu-id="75cf1-180">Identyfikator strefy czasowej wystąpienia, które ma być ustawiane.</span><span class="sxs-lookup"><span data-stu-id="75cf1-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="75cf1-181">Lista identyfikatorów strefy czasowej jest ujawniona w widoku sys.time_zone_info języka (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="75cf1-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="75cf1-182">— VCore</span><span class="sxs-lookup"><span data-stu-id="75cf1-182">-VCore</span></span>
<span data-ttu-id="75cf1-183">Określenie, ile vcore ma skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="75cf1-183">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf1-184">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75cf1-184">-Confirm</span></span>
<span data-ttu-id="75cf1-185">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="75cf1-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cf1-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cf1-186">-WhatIf</span></span>
<span data-ttu-id="75cf1-187">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75cf1-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75cf1-188">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="75cf1-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cf1-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cf1-189">CommonParameters</span></span>
<span data-ttu-id="75cf1-190">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cf1-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cf1-191">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75cf1-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cf1-192">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75cf1-192">INPUTS</span></span>

### <span data-ttu-id="75cf1-193">Brak</span><span class="sxs-lookup"><span data-stu-id="75cf1-193">None</span></span>

## <span data-ttu-id="75cf1-194">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75cf1-194">OUTPUTS</span></span>

### <span data-ttu-id="75cf1-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="75cf1-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="75cf1-196">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75cf1-196">NOTES</span></span>

## <span data-ttu-id="75cf1-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75cf1-197">RELATED LINKS</span></span>
