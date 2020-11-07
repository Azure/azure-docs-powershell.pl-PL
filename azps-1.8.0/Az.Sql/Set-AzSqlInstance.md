---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: ad98b764eac08c9fb1f6d3dd367d78ca1b5d45d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707738"
---
# <span data-ttu-id="43ce1-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="43ce1-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="43ce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="43ce1-103">Ustawia właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="43ce1-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="43ce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43ce1-104">SYNTAX</span></span>

### <span data-ttu-id="43ce1-105">SetInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43ce1-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ce1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="43ce1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ce1-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="43ce1-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ce1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43ce1-108">DESCRIPTION</span></span>
<span data-ttu-id="43ce1-109">Polecenie cmdlet **Set-AzSqlInstance** modyfikuje właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="43ce1-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="43ce1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43ce1-110">EXAMPLES</span></span>

### <span data-ttu-id="43ce1-111">Przykład 1: Ustawianie istniejącego wystąpienia przy użyciu nowych wartości dla-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="43ce1-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
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
```

<span data-ttu-id="43ce1-112">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="43ce1-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="43ce1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43ce1-113">PARAMETERS</span></span>

### <span data-ttu-id="43ce1-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="43ce1-114">-AdministratorPassword</span></span>
<span data-ttu-id="43ce1-115">Nowe hasło administratora SQL dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-115">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="43ce1-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="43ce1-116">-AssignIdentity</span></span>
<span data-ttu-id="43ce1-117">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia, aby móc korzystać z usług zarządzania kluczami, takich jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43ce1-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="43ce1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ce1-118">-DefaultProfile</span></span>
<span data-ttu-id="43ce1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43ce1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ce1-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="43ce1-120">-Edition</span></span>
<span data-ttu-id="43ce1-121">Wersja do przypisania do wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="43ce1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="43ce1-122">-Force</span></span>
<span data-ttu-id="43ce1-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="43ce1-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="43ce1-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43ce1-124">-InputObject</span></span>
<span data-ttu-id="43ce1-125">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="43ce1-125">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="43ce1-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="43ce1-126">-LicenseType</span></span>
<span data-ttu-id="43ce1-127">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="43ce1-127">Determines which License Type to use.</span></span> <span data-ttu-id="43ce1-128">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="43ce1-128">Possible values are:</span></span>
- <span data-ttu-id="43ce1-129">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43ce1-129">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="43ce1-130">Cena usług zarządzanych wystąpień będzie dyskontowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43ce1-130">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="43ce1-131">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="43ce1-131">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="43ce1-132">Cena usług zarządzanych wystąpień będzie uwzględniać nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43ce1-132">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="43ce1-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43ce1-133">-Name</span></span>
<span data-ttu-id="43ce1-134">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-134">Instance name.</span></span>

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

### <span data-ttu-id="43ce1-135">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="43ce1-135">-ProxyOverride</span></span>
<span data-ttu-id="43ce1-136">Typ połączenia służący do nawiązywania połączenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="43ce1-136">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="43ce1-137">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="43ce1-137">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="43ce1-138">Czy punkt końcowy danych publicznych jest włączony dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-138">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="43ce1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ce1-139">-ResourceGroupName</span></span>
<span data-ttu-id="43ce1-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43ce1-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="43ce1-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43ce1-141">-ResourceId</span></span>
<span data-ttu-id="43ce1-142">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="43ce1-142">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="43ce1-143">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="43ce1-143">-StorageSizeInGB</span></span>
<span data-ttu-id="43ce1-144">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="43ce1-144">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="43ce1-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="43ce1-145">-Tag</span></span>
<span data-ttu-id="43ce1-146">Znaczniki, które mają zostać skojarzone z instancją.</span><span class="sxs-lookup"><span data-stu-id="43ce1-146">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="43ce1-147">-VCore</span><span class="sxs-lookup"><span data-stu-id="43ce1-147">-VCore</span></span>
<span data-ttu-id="43ce1-148">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="43ce1-148">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="43ce1-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43ce1-149">-Confirm</span></span>
<span data-ttu-id="43ce1-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ce1-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ce1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ce1-151">-WhatIf</span></span>
<span data-ttu-id="43ce1-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ce1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ce1-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43ce1-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ce1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ce1-154">CommonParameters</span></span>
<span data-ttu-id="43ce1-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ce1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ce1-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43ce1-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ce1-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43ce1-157">INPUTS</span></span>

### <span data-ttu-id="43ce1-158">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="43ce1-158">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="43ce1-159">System. String</span><span class="sxs-lookup"><span data-stu-id="43ce1-159">System.String</span></span>

## <span data-ttu-id="43ce1-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43ce1-160">OUTPUTS</span></span>

### <span data-ttu-id="43ce1-161">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="43ce1-161">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="43ce1-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43ce1-162">NOTES</span></span>

## <span data-ttu-id="43ce1-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43ce1-163">RELATED LINKS</span></span>
