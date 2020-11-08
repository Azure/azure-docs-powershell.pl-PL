---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220269"
---
# <span data-ttu-id="d518f-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d518f-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="d518f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d518f-102">SYNOPSIS</span></span>
<span data-ttu-id="d518f-103">Ustawia właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d518f-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d518f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d518f-104">SYNTAX</span></span>

### <span data-ttu-id="d518f-105">SetInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d518f-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d518f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d518f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d518f-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d518f-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d518f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d518f-108">DESCRIPTION</span></span>
<span data-ttu-id="d518f-109">Polecenie cmdlet **Set-AzSqlInstance** modyfikuje właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d518f-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="d518f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d518f-110">EXAMPLES</span></span>

### <span data-ttu-id="d518f-111">Przykład 1: Ustawianie istniejącego wystąpienia za pomocą nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore i-Edition</span><span class="sxs-lookup"><span data-stu-id="d518f-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="d518f-112">Przykład 2: Zmienianie wygenerowania sprzętu wystąpienia przy użyciu nowej wartości dla parametru-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d518f-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="d518f-113">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="d518f-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="d518f-114">Przykład 3: Ustawianie istniejącego wystąpienia przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore dla wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="d518f-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="d518f-115">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore dla wystąpienia w puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="d518f-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="d518f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d518f-116">PARAMETERS</span></span>

### <span data-ttu-id="d518f-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="d518f-117">-AdministratorPassword</span></span>
<span data-ttu-id="d518f-118">Nowe hasło administratora SQL dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d518f-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="d518f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d518f-119">-AsJob</span></span>
<span data-ttu-id="d518f-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d518f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d518f-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d518f-121">-AssignIdentity</span></span>
<span data-ttu-id="d518f-122">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia, aby móc korzystać z usług zarządzania kluczami, takich jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d518f-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d518f-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d518f-123">-ComputeGeneration</span></span>
<span data-ttu-id="d518f-124">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d518f-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="d518f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d518f-125">-DefaultProfile</span></span>
<span data-ttu-id="d518f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d518f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d518f-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="d518f-127">-Edition</span></span>
<span data-ttu-id="d518f-128">Wersja do przypisania do wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d518f-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="d518f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d518f-129">-Force</span></span>
<span data-ttu-id="d518f-130">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="d518f-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d518f-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d518f-131">-InputObject</span></span>
<span data-ttu-id="d518f-132">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d518f-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="d518f-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="d518f-133">-InstancePoolName</span></span>
<span data-ttu-id="d518f-134">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="d518f-134">The instance pool name.</span></span>

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

### <span data-ttu-id="d518f-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d518f-135">-LicenseType</span></span>
<span data-ttu-id="d518f-136">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d518f-136">Determines which License Type to use.</span></span> <span data-ttu-id="d518f-137">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="d518f-137">Possible values are:</span></span>
- <span data-ttu-id="d518f-138">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d518f-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="d518f-139">Cena usług zarządzanych wystąpień będzie dyskontowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d518f-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="d518f-140">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="d518f-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="d518f-141">Cena usług zarządzanych wystąpień będzie uwzględniać nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d518f-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="d518f-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d518f-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="d518f-143">Minimalna wersja TLS do wymuszenia dla wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="d518f-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="d518f-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d518f-144">-Name</span></span>
<span data-ttu-id="d518f-145">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d518f-145">Instance name.</span></span>

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

### <span data-ttu-id="d518f-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="d518f-146">-ProxyOverride</span></span>
<span data-ttu-id="d518f-147">Typ połączenia służący do nawiązywania połączenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="d518f-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="d518f-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="d518f-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="d518f-149">Czy punkt końcowy danych publicznych jest włączony dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d518f-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="d518f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d518f-150">-ResourceGroupName</span></span>
<span data-ttu-id="d518f-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d518f-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="d518f-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d518f-152">-ResourceId</span></span>
<span data-ttu-id="d518f-153">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d518f-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="d518f-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d518f-154">-StorageSizeInGB</span></span>
<span data-ttu-id="d518f-155">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="d518f-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="d518f-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="d518f-156">-Tag</span></span>
<span data-ttu-id="d518f-157">Znaczniki, które mają zostać skojarzone z instancją.</span><span class="sxs-lookup"><span data-stu-id="d518f-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="d518f-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="d518f-158">-VCore</span></span>
<span data-ttu-id="d518f-159">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="d518f-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="d518f-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d518f-160">-Confirm</span></span>
<span data-ttu-id="d518f-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d518f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d518f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d518f-162">-WhatIf</span></span>
<span data-ttu-id="d518f-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d518f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d518f-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d518f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d518f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d518f-165">CommonParameters</span></span>
<span data-ttu-id="d518f-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d518f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d518f-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d518f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d518f-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d518f-168">INPUTS</span></span>

### <span data-ttu-id="d518f-169">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d518f-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d518f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="d518f-170">System.String</span></span>

## <span data-ttu-id="d518f-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d518f-171">OUTPUTS</span></span>

### <span data-ttu-id="d518f-172">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d518f-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d518f-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d518f-173">NOTES</span></span>

## <span data-ttu-id="d518f-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d518f-174">RELATED LINKS</span></span>
