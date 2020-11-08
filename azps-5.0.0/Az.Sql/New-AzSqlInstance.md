---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225636"
---
# <span data-ttu-id="1f821-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1f821-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="1f821-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f821-102">SYNOPSIS</span></span>
<span data-ttu-id="1f821-103">Tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1f821-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="1f821-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f821-104">SYNTAX</span></span>

### <span data-ttu-id="1f821-105">NewByEditionAndComputeGenerationParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f821-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f821-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f821-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f821-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f821-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f821-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="1f821-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f821-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1f821-109">DESCRIPTION</span></span>
<span data-ttu-id="1f821-110">Polecenie cmdlet **New-AzSqlInstance** tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1f821-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="1f821-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f821-111">EXAMPLES</span></span>

### <span data-ttu-id="1f821-112">Przykład 1. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1f821-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="1f821-113">To polecenie tworzy nowe wystąpienie przy użyciu parametru SkuName.</span><span class="sxs-lookup"><span data-stu-id="1f821-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="1f821-114">Przykład 2: Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1f821-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="1f821-115">To polecenie tworzy nowe wystąpienie za pomocą parametrów wersja i ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="1f821-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="1f821-116">Przykład 3: Tworzenie nowego wystąpienia w puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="1f821-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="1f821-117">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="1f821-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="1f821-118">Przykład 4: Tworzenie nowego wystąpienia w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="1f821-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="1f821-119">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="1f821-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="1f821-120">Przykład 5: Tworzenie nowego wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="1f821-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="1f821-121">To polecenie tworzy nowe wystąpienie w puli wystąpień o nazwie instancePool0</span><span class="sxs-lookup"><span data-stu-id="1f821-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="1f821-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f821-122">PARAMETERS</span></span>

### <span data-ttu-id="1f821-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="1f821-123">-AdministratorCredential</span></span>
<span data-ttu-id="1f821-124">Poświadczenie uwierzytelniania SQL wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1f821-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="1f821-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f821-125">-AsJob</span></span>
<span data-ttu-id="1f821-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f821-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f821-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1f821-127">-AssignIdentity</span></span>
<span data-ttu-id="1f821-128">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia zarządzanego, które ma być używane z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f821-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1f821-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="1f821-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="1f821-130">Nadmiarowość miejsca do magazynowania kopii zapasowej używana do przechowywania kopii zapasowych dla wystąpienia zarządzanego w usłudze SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1f821-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="1f821-131">Opcje: lokalne, strefy i geo</span><span class="sxs-lookup"><span data-stu-id="1f821-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="1f821-132">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="1f821-132">-Collation</span></span>
<span data-ttu-id="1f821-133">Sortowanie wystąpienia zarządzanego przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1f821-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="1f821-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="1f821-134">-ComputeGeneration</span></span>
<span data-ttu-id="1f821-135">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1f821-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="1f821-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f821-136">-DefaultProfile</span></span>
<span data-ttu-id="1f821-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f821-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f821-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="1f821-138">-DnsZonePartner</span></span>
<span data-ttu-id="1f821-139">Identyfikator zasobu serwera zarządzanego przez partnera umożliwiający dziedziczenie właściwości DnsZone w celu utworzenia wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="1f821-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="1f821-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="1f821-140">-Edition</span></span>
<span data-ttu-id="1f821-141">Wersja dla tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1f821-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="1f821-142">-Force</span><span class="sxs-lookup"><span data-stu-id="1f821-142">-Force</span></span>
<span data-ttu-id="1f821-143">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="1f821-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1f821-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="1f821-144">-InstancePool</span></span>
<span data-ttu-id="1f821-145">Obiekt nadrzędny puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="1f821-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="1f821-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="1f821-146">-InstancePoolName</span></span>
<span data-ttu-id="1f821-147">Pula wystąpień, w której ma zostać umieszczone to wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="1f821-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="1f821-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="1f821-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="1f821-149">Identyfikator zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="1f821-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="1f821-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1f821-150">-LicenseType</span></span>
<span data-ttu-id="1f821-151">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1f821-151">Determines which License Type to use.</span></span> <span data-ttu-id="1f821-152">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="1f821-152">Possible values are:</span></span>
- <span data-ttu-id="1f821-153">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f821-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="1f821-154">Cena usług zarządzanych wystąpień będzie dyskontowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f821-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="1f821-155">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="1f821-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="1f821-156">Cena usług zarządzanych wystąpień będzie uwzględniać nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f821-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="1f821-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1f821-157">-Location</span></span>
<span data-ttu-id="1f821-158">Lokalizacja, w której ma zostać utworzone wystąpienie</span><span class="sxs-lookup"><span data-stu-id="1f821-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="1f821-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1f821-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="1f821-160">Minimalna wersja TLS do wymuszenia dla wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="1f821-160">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="1f821-161">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f821-161">-Name</span></span>
<span data-ttu-id="1f821-162">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1f821-162">Instance name.</span></span>

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

### <span data-ttu-id="1f821-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="1f821-163">-ProxyOverride</span></span>
<span data-ttu-id="1f821-164">Typ połączenia służący do nawiązywania połączenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="1f821-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="1f821-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="1f821-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="1f821-166">Czy punkt końcowy danych publicznych jest włączony dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1f821-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="1f821-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f821-167">-ResourceGroupName</span></span>
<span data-ttu-id="1f821-168">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f821-168">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f821-169">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1f821-169">-SkuName</span></span>
<span data-ttu-id="1f821-170">Nazwa SKU wystąpienia, na przykład "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="1f821-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="1f821-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1f821-171">-StorageSizeInGB</span></span>
<span data-ttu-id="1f821-172">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="1f821-172">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="1f821-173">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1f821-173">-SubnetId</span></span>
<span data-ttu-id="1f821-174">Identyfikator podsieci, który ma zostać użyty do utworzenia wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1f821-174">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="1f821-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f821-175">-Tag</span></span>
<span data-ttu-id="1f821-176">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="1f821-176">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="1f821-177">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="1f821-177">-TimezoneId</span></span>
<span data-ttu-id="1f821-178">Identyfikator strefy czasowej dla wystąpienia, które należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="1f821-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="1f821-179">Lista identyfikatorów stref czasowych jest udostępniana za pośrednictwem widoku sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="1f821-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="1f821-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="1f821-180">-VCore</span></span>
<span data-ttu-id="1f821-181">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="1f821-181">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="1f821-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f821-182">-Confirm</span></span>
<span data-ttu-id="1f821-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f821-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f821-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f821-184">-WhatIf</span></span>
<span data-ttu-id="1f821-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f821-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f821-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f821-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f821-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f821-187">CommonParameters</span></span>
<span data-ttu-id="1f821-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f821-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f821-189">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f821-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f821-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f821-190">INPUTS</span></span>

### <span data-ttu-id="1f821-191">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f821-191">None</span></span>

## <span data-ttu-id="1f821-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f821-192">OUTPUTS</span></span>

### <span data-ttu-id="1f821-193">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1f821-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="1f821-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f821-194">NOTES</span></span>

## <span data-ttu-id="1f821-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f821-195">RELATED LINKS</span></span>
