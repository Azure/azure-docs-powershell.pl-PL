---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015866"
---
# <span data-ttu-id="a09cf-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a09cf-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="a09cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a09cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a09cf-103">Ustawia właściwości zarządzanego wystąpienia usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a09cf-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a09cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a09cf-104">SYNTAX</span></span>

### <span data-ttu-id="a09cf-105">SetInstanceFromInputParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a09cf-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09cf-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a09cf-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09cf-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a09cf-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09cf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a09cf-108">DESCRIPTION</span></span>
<span data-ttu-id="a09cf-109">Polecenie **cmdlet Set-AzSqlInstance** modyfikuje właściwości wystąpienia zarządzanego przez usługę Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a09cf-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="a09cf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a09cf-110">EXAMPLES</span></span>

### <span data-ttu-id="a09cf-111">Przykład 1. Ustawianie istniejącego wystąpienia przy użyciu nowych wartości dla wartości -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore i -Edition</span><span class="sxs-lookup"><span data-stu-id="a09cf-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="a09cf-112">Przykład 2. Zmienianie generowania sprzętu istniejącego wystąpienia przy użyciu nowej wartości dla -Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="a09cf-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="a09cf-113">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości dla wartości -AdministratorPassword, -LicenseType, -StorageSizeInGB i -VCore</span><span class="sxs-lookup"><span data-stu-id="a09cf-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="a09cf-114">Przykład 3. Ustawianie istniejącego wystąpienia przy użyciu nowych wartości dla wartości -AdministratorPassword, -LicenseType, -StorageSizeInGB i -VCore dla wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="a09cf-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="a09cf-115">To polecenie ustawia istniejące wystąpienie, używając nowych wartości dla wartości -AdministratorPassword, -LicenseType, -StorageSizeInGB i -VCore dla wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="a09cf-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="a09cf-116">Przykład 4. Aktualizowanie konfiguracji konserwacji dla istniejącego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a09cf-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="a09cf-117">To polecenie aktualizuje istniejące wystąpienie za pomocą funkcji konfiguracji MI_2</span><span class="sxs-lookup"><span data-stu-id="a09cf-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="a09cf-118">Przykład 5. Usuwanie konfiguracji konserwacji z istniejącego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a09cf-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="a09cf-119">To polecenie powoduje zresetowanie konfiguracji konserwacji do domyślnej dla istniejącego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a09cf-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="a09cf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a09cf-120">PARAMETERS</span></span>

### <span data-ttu-id="a09cf-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="a09cf-121">-AdministratorPassword</span></span>
<span data-ttu-id="a09cf-122">Nowe hasło administratora języka SQL dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a09cf-122">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="a09cf-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a09cf-123">-AsJob</span></span>
<span data-ttu-id="a09cf-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a09cf-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a09cf-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a09cf-125">-AssignIdentity</span></span>
<span data-ttu-id="a09cf-126">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia do używania z usługami zarządzania kluczami, np. Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a09cf-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a09cf-127">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="a09cf-127">-ComputeGeneration</span></span>
<span data-ttu-id="a09cf-128">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a09cf-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="a09cf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09cf-129">-DefaultProfile</span></span>
<span data-ttu-id="a09cf-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a09cf-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09cf-131">— wersja</span><span class="sxs-lookup"><span data-stu-id="a09cf-131">-Edition</span></span>
<span data-ttu-id="a09cf-132">Wersja do przypisania do wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a09cf-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="a09cf-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a09cf-133">-Force</span></span>
<span data-ttu-id="a09cf-134">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="a09cf-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a09cf-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a09cf-135">-InputObject</span></span>
<span data-ttu-id="a09cf-136">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a09cf-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="a09cf-137">-InstancePoolName</span></span>
<span data-ttu-id="a09cf-138">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="a09cf-138">The instance pool name.</span></span>

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

### <span data-ttu-id="a09cf-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a09cf-139">-LicenseType</span></span>
<span data-ttu-id="a09cf-140">Określenie typu licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="a09cf-140">Determines which License Type to use.</span></span> <span data-ttu-id="a09cf-141">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="a09cf-141">Possible values are:</span></span>
- <span data-ttu-id="a09cf-142">Cena Bazowa — zastosowano rabat w ramach korzyści hybrydowej platformy Azure (AHB) dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a09cf-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a09cf-143">Cena usługi zarządzanego wystąpienia zostanie zdyskoowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a09cf-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a09cf-144">Cena rabatu z rabatem na usługę Azure Hybrid Benefit (AHB) dla istniejących właścicieli licencji programu SQL Server nie jest stosowana.</span><span class="sxs-lookup"><span data-stu-id="a09cf-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a09cf-145">Cena usługi zarządzanego wystąpienia będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a09cf-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="a09cf-146">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a09cf-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="a09cf-147">Identyfikator konfiguracji konserwacji dla wystąpienia zarządzanego platformy Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="a09cf-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="a09cf-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a09cf-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="a09cf-149">Minimalna wersja TLS wymuszana dla wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="a09cf-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="a09cf-150">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a09cf-150">-Name</span></span>
<span data-ttu-id="a09cf-151">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a09cf-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="a09cf-152">-ProxyOverride</span></span>
<span data-ttu-id="a09cf-153">Typ połączenia używany do łączenia się z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="a09cf-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="a09cf-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="a09cf-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="a09cf-155">Czy dla wystąpienia jest włączony publiczny punkt końcowy danych.</span><span class="sxs-lookup"><span data-stu-id="a09cf-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09cf-156">-ResourceGroupName</span></span>
<span data-ttu-id="a09cf-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a09cf-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a09cf-158">-ResourceId</span></span>
<span data-ttu-id="a09cf-159">Identyfikator wystąpienia zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a09cf-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-160">- StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a09cf-160">-StorageSizeInGB</span></span>
<span data-ttu-id="a09cf-161">Określa, ile miejsca do magazynowania należy skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="a09cf-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-162">— Tag</span><span class="sxs-lookup"><span data-stu-id="a09cf-162">-Tag</span></span>
<span data-ttu-id="a09cf-163">Tagi do skojarzenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="a09cf-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="a09cf-164">— VCore</span><span class="sxs-lookup"><span data-stu-id="a09cf-164">-VCore</span></span>
<span data-ttu-id="a09cf-165">Określenie, ile vcore ma skojarzyć z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="a09cf-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09cf-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a09cf-166">-Confirm</span></span>
<span data-ttu-id="a09cf-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a09cf-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09cf-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09cf-168">-WhatIf</span></span>
<span data-ttu-id="a09cf-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a09cf-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09cf-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a09cf-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09cf-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09cf-171">CommonParameters</span></span>
<span data-ttu-id="a09cf-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09cf-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09cf-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a09cf-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09cf-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a09cf-174">INPUTS</span></span>

### <span data-ttu-id="a09cf-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a09cf-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="a09cf-176">System.String</span><span class="sxs-lookup"><span data-stu-id="a09cf-176">System.String</span></span>

## <span data-ttu-id="a09cf-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a09cf-177">OUTPUTS</span></span>

### <span data-ttu-id="a09cf-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a09cf-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a09cf-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a09cf-179">NOTES</span></span>

## <span data-ttu-id="a09cf-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a09cf-180">RELATED LINKS</span></span>
