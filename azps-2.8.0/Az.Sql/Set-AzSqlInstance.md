---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887230"
---
# <span data-ttu-id="3af95-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3af95-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="3af95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3af95-102">SYNOPSIS</span></span>
<span data-ttu-id="3af95-103">Ustawia właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3af95-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3af95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3af95-104">SYNTAX</span></span>

### <span data-ttu-id="3af95-105">SetInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3af95-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af95-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="3af95-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af95-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="3af95-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af95-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3af95-108">DESCRIPTION</span></span>
<span data-ttu-id="3af95-109">Polecenie cmdlet **Set-AzSqlInstance** modyfikuje właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3af95-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3af95-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3af95-110">EXAMPLES</span></span>

### <span data-ttu-id="3af95-111">Przykład 1: Ustawianie istniejącego wystąpienia przy użyciu nowych wartości dla-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="3af95-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="3af95-112">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="3af95-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="3af95-113">Przykład 2: Ustawianie istniejącego wystąpienia przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore dla wystąpienia w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="3af95-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="3af95-114">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore dla wystąpienia w puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3af95-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="3af95-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3af95-115">PARAMETERS</span></span>

### <span data-ttu-id="3af95-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="3af95-116">-AdministratorPassword</span></span>
<span data-ttu-id="3af95-117">Nowe hasło administratora SQL dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3af95-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="3af95-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3af95-118">-AssignIdentity</span></span>
<span data-ttu-id="3af95-119">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia, aby móc korzystać z usług zarządzania kluczami, takich jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3af95-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3af95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af95-120">-DefaultProfile</span></span>
<span data-ttu-id="3af95-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3af95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3af95-122">-Edition</span><span class="sxs-lookup"><span data-stu-id="3af95-122">-Edition</span></span>
<span data-ttu-id="3af95-123">Wersja do przypisania do wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3af95-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="3af95-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3af95-124">-Force</span></span>
<span data-ttu-id="3af95-125">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="3af95-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3af95-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3af95-126">-InputObject</span></span>
<span data-ttu-id="3af95-127">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3af95-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="3af95-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3af95-128">-InstancePoolName</span></span>
<span data-ttu-id="3af95-129">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="3af95-129">The instance pool name.</span></span>

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

### <span data-ttu-id="3af95-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3af95-130">-LicenseType</span></span>
<span data-ttu-id="3af95-131">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3af95-131">Determines which License Type to use.</span></span> <span data-ttu-id="3af95-132">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="3af95-132">Possible values are:</span></span>
- <span data-ttu-id="3af95-133">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3af95-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3af95-134">Cena usług zarządzanych wystąpień będzie dyskontowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3af95-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3af95-135">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="3af95-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3af95-136">Cena usług zarządzanych wystąpień będzie uwzględniać nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3af95-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3af95-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3af95-137">-Name</span></span>
<span data-ttu-id="3af95-138">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3af95-138">Instance name.</span></span>

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

### <span data-ttu-id="3af95-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3af95-139">-ProxyOverride</span></span>
<span data-ttu-id="3af95-140">Typ połączenia służący do nawiązywania połączenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="3af95-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3af95-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3af95-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3af95-142">Czy punkt końcowy danych publicznych jest włączony dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3af95-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3af95-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af95-143">-ResourceGroupName</span></span>
<span data-ttu-id="3af95-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3af95-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="3af95-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3af95-145">-ResourceId</span></span>
<span data-ttu-id="3af95-146">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3af95-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="3af95-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3af95-147">-StorageSizeInGB</span></span>
<span data-ttu-id="3af95-148">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="3af95-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="3af95-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="3af95-149">-Tag</span></span>
<span data-ttu-id="3af95-150">Znaczniki, które mają zostać skojarzone z instancją.</span><span class="sxs-lookup"><span data-stu-id="3af95-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="3af95-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="3af95-151">-VCore</span></span>
<span data-ttu-id="3af95-152">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="3af95-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="3af95-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3af95-153">-Confirm</span></span>
<span data-ttu-id="3af95-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af95-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af95-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af95-155">-WhatIf</span></span>
<span data-ttu-id="3af95-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af95-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af95-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3af95-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af95-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af95-158">CommonParameters</span></span>
<span data-ttu-id="3af95-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af95-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af95-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3af95-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af95-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3af95-161">INPUTS</span></span>

### <span data-ttu-id="3af95-162">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3af95-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="3af95-163">System. String</span><span class="sxs-lookup"><span data-stu-id="3af95-163">System.String</span></span>

## <span data-ttu-id="3af95-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3af95-164">OUTPUTS</span></span>

### <span data-ttu-id="3af95-165">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3af95-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3af95-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3af95-166">NOTES</span></span>

## <span data-ttu-id="3af95-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3af95-167">RELATED LINKS</span></span>
