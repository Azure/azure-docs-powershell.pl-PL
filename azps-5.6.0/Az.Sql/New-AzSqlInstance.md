---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970202"
---
# <span data-ttu-id="3a716-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a716-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="3a716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a716-102">SYNOPSIS</span></span>
<span data-ttu-id="3a716-103">Tworzy wystąpienie zarządzane usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3a716-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3a716-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a716-104">SYNTAX</span></span>

### <span data-ttu-id="3a716-105">NewByEditionAndComputeGenerParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="3a716-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a716-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a716-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a716-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a716-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a716-108">NewBySkuNameParameterSetParameters</span><span class="sxs-lookup"><span data-stu-id="3a716-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a716-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a716-109">DESCRIPTION</span></span>
<span data-ttu-id="3a716-110">Polecenie **cmdlet New-AzSqlInstance** tworzy wystąpienie zarządzane przez usługę Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3a716-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3a716-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a716-111">EXAMPLES</span></span>

### <span data-ttu-id="3a716-112">Przykład 1. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="3a716-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="3a716-113">To polecenie tworzy nowe wystąpienie przy użyciu parametru SKUName.</span><span class="sxs-lookup"><span data-stu-id="3a716-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="3a716-114">Przykład 2. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="3a716-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="3a716-115">To polecenie tworzy nowe wystąpienie przy użyciu parametrów Edition i ComputeGeneracja.</span><span class="sxs-lookup"><span data-stu-id="3a716-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="3a716-116">Przykład 3. Tworzenie nowego wystąpienia w puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="3a716-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="3a716-117">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3a716-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="3a716-118">Przykład 4. Tworzenie nowego wystąpienia w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="3a716-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="3a716-119">To polecenie tworzy nowe wystąpienie w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3a716-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="3a716-120">Przykład 5. Tworzenie nowego wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="3a716-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="3a716-121">To polecenie tworzy nowe wystąpienie w puli wystąpień z wystąpieniem nazwPool0</span><span class="sxs-lookup"><span data-stu-id="3a716-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="3a716-122">Przykład 6. Tworzenie nowego wystąpienia z konfiguracją konserwacji</span><span class="sxs-lookup"><span data-stu-id="3a716-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="3a716-123">To polecenie tworzy nowe wystąpienie z konfiguracją konserwacji MI_2</span><span class="sxs-lookup"><span data-stu-id="3a716-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="3a716-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a716-124">PARAMETERS</span></span>

### <span data-ttu-id="3a716-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="3a716-125">-AdministratorCredential</span></span>
<span data-ttu-id="3a716-126">Poświadczenia uwierzytelniania SQL wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a716-126">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="3a716-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3a716-127">-AsJob</span></span>
<span data-ttu-id="3a716-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3a716-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a716-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3a716-129">-AssignIdentity</span></span>
<span data-ttu-id="3a716-130">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego zarządzanego wystąpienia do użycia z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3a716-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3a716-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3a716-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3a716-132">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla wystąpienia zarządzanego platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="3a716-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="3a716-133">Dostępne opcje: Lokalny, Strefowy i Geolokalizacji</span><span class="sxs-lookup"><span data-stu-id="3a716-133">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="3a716-134">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="3a716-134">-Collation</span></span>
<span data-ttu-id="3a716-135">Sortowanie wystąpienia zarządzanego przez język Azure SQL do użycia.</span><span class="sxs-lookup"><span data-stu-id="3a716-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="3a716-136">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="3a716-136">-ComputeGeneration</span></span>
<span data-ttu-id="3a716-137">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a716-137">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="3a716-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a716-138">-DefaultProfile</span></span>
<span data-ttu-id="3a716-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a716-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a716-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="3a716-140">-DnsZonePartner</span></span>
<span data-ttu-id="3a716-141">Identyfikator zasobu zarządzanego serwera partnerskiego do dziedziczenia właściwości DnsZone po utworzeniu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="3a716-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="3a716-142">— wersja</span><span class="sxs-lookup"><span data-stu-id="3a716-142">-Edition</span></span>
<span data-ttu-id="3a716-143">Wersja tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a716-143">The edition for the instance.</span></span>

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

### <span data-ttu-id="3a716-144">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3a716-144">-Force</span></span>
<span data-ttu-id="3a716-145">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="3a716-145">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3a716-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="3a716-146">-InstancePool</span></span>
<span data-ttu-id="3a716-147">Obiekt nadrzędny puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3a716-147">The instance pool parent object.</span></span>

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

### <span data-ttu-id="3a716-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3a716-148">-InstancePoolName</span></span>
<span data-ttu-id="3a716-149">Pula wystąpień, w którym należy umieścić to wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="3a716-149">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="3a716-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="3a716-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="3a716-151">Identyfikator zasobu puli wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a716-151">The instance pool resource id.</span></span>

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

### <span data-ttu-id="3a716-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3a716-152">-LicenseType</span></span>
<span data-ttu-id="3a716-153">Określenie typu licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="3a716-153">Determines which License Type to use.</span></span> <span data-ttu-id="3a716-154">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="3a716-154">Possible values are:</span></span>
- <span data-ttu-id="3a716-155">Cena Bazowa — zastosowano rabat w ramach korzyści hybrydowej platformy Azure (AHB) dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a716-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3a716-156">Cena usługi zarządzanego wystąpienia zostanie zdyskoowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a716-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3a716-157">Cena rabatu z rabatem na usługę Azure Hybrid Benefit (AHB) dla istniejących właścicieli licencji programu SQL Server nie jest stosowana.</span><span class="sxs-lookup"><span data-stu-id="3a716-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3a716-158">Cena usługi zarządzanego wystąpienia będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a716-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3a716-159">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3a716-159">-Location</span></span>
<span data-ttu-id="3a716-160">Lokalizacja, w której należy utworzyć wystąpienie</span><span class="sxs-lookup"><span data-stu-id="3a716-160">The location in which to create the instance</span></span>

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

### <span data-ttu-id="3a716-161">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3a716-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="3a716-162">Identyfikator konfiguracji konserwacji dla wystąpienia zarządzanego platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="3a716-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="3a716-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3a716-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="3a716-164">Minimalna wersja TLS wymuszana dla wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="3a716-164">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="3a716-165">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a716-165">-Name</span></span>
<span data-ttu-id="3a716-166">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a716-166">Instance name.</span></span>

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

### <span data-ttu-id="3a716-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3a716-167">-ProxyOverride</span></span>
<span data-ttu-id="3a716-168">Typ połączenia używany do łączenia się z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="3a716-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3a716-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3a716-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3a716-170">Czy dla wystąpienia jest włączony publiczny punkt końcowy danych.</span><span class="sxs-lookup"><span data-stu-id="3a716-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3a716-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a716-171">-ResourceGroupName</span></span>
<span data-ttu-id="3a716-172">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a716-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a716-173">-SKUName</span><span class="sxs-lookup"><span data-stu-id="3a716-173">-SkuName</span></span>
<span data-ttu-id="3a716-174">Nazwa SKU wystąpienia, na przykład "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="3a716-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="3a716-175">- StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3a716-175">-StorageSizeInGB</span></span>
<span data-ttu-id="3a716-176">Określa, ile miejsca do magazynowania należy skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="3a716-176">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="3a716-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3a716-177">-SubnetId</span></span>
<span data-ttu-id="3a716-178">Identyfikator podsieci do użycia podczas tworzenia wystąpień</span><span class="sxs-lookup"><span data-stu-id="3a716-178">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="3a716-179">— Tag</span><span class="sxs-lookup"><span data-stu-id="3a716-179">-Tag</span></span>
<span data-ttu-id="3a716-180">Tagi do skojarzenia z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="3a716-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="3a716-181">- TimezoneId</span><span class="sxs-lookup"><span data-stu-id="3a716-181">-TimezoneId</span></span>
<span data-ttu-id="3a716-182">Identyfikator strefy czasowej wystąpienia, które ma być ustawiane.</span><span class="sxs-lookup"><span data-stu-id="3a716-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="3a716-183">Lista identyfikatorów strefy czasowej jest ujawniona w widoku sys.time_zone_info języka (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="3a716-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="3a716-184">— VCore</span><span class="sxs-lookup"><span data-stu-id="3a716-184">-VCore</span></span>
<span data-ttu-id="3a716-185">Określenie, ile vcore ma skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="3a716-185">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="3a716-186">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a716-186">-Confirm</span></span>
<span data-ttu-id="3a716-187">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a716-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a716-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a716-188">-WhatIf</span></span>
<span data-ttu-id="3a716-189">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a716-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a716-190">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a716-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a716-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a716-191">CommonParameters</span></span>
<span data-ttu-id="3a716-192">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a716-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a716-193">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a716-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a716-194">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a716-194">INPUTS</span></span>

### <span data-ttu-id="3a716-195">Brak</span><span class="sxs-lookup"><span data-stu-id="3a716-195">None</span></span>

## <span data-ttu-id="3a716-196">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a716-196">OUTPUTS</span></span>

### <span data-ttu-id="3a716-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3a716-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3a716-198">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a716-198">NOTES</span></span>

## <span data-ttu-id="3a716-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a716-199">RELATED LINKS</span></span>
