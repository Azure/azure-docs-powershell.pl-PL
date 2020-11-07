---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707857"
---
# <span data-ttu-id="4e73a-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4e73a-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="4e73a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e73a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e73a-103">Tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4e73a-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="4e73a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e73a-104">SYNTAX</span></span>

### <span data-ttu-id="4e73a-105">NewByEditionAndComputeGenerationParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e73a-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e73a-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="4e73a-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e73a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4e73a-107">DESCRIPTION</span></span>
<span data-ttu-id="4e73a-108">Polecenie cmdlet **New-AzSqlInstance** tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4e73a-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="4e73a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e73a-109">EXAMPLES</span></span>

### <span data-ttu-id="4e73a-110">Przykład 1. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4e73a-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="4e73a-111">To polecenie tworzy nowe wystąpienie przy użyciu parametrów wersja i ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="4e73a-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="4e73a-112">Przykład 2: Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4e73a-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="4e73a-113">To polecenie tworzy nowe wystąpienie za pomocą parametrów wersja i ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="4e73a-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="4e73a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e73a-114">PARAMETERS</span></span>

### <span data-ttu-id="4e73a-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="4e73a-115">-AdministratorCredential</span></span>
<span data-ttu-id="4e73a-116">Poświadczenie uwierzytelniania SQL wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4e73a-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="4e73a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e73a-117">-AsJob</span></span>
<span data-ttu-id="4e73a-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4e73a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e73a-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4e73a-119">-AssignIdentity</span></span>
<span data-ttu-id="4e73a-120">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia zarządzanego, które ma być używane z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4e73a-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4e73a-121">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="4e73a-121">-Collation</span></span>
<span data-ttu-id="4e73a-122">Sortowanie wystąpienia zarządzanego przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4e73a-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="4e73a-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4e73a-123">-ComputeGeneration</span></span>
<span data-ttu-id="4e73a-124">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4e73a-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="4e73a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e73a-125">-DefaultProfile</span></span>
<span data-ttu-id="4e73a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e73a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e73a-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="4e73a-127">-Edition</span></span>
<span data-ttu-id="4e73a-128">Wersja dla tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4e73a-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="4e73a-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4e73a-129">-LicenseType</span></span>
<span data-ttu-id="4e73a-130">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4e73a-130">Determines which License Type to use.</span></span> <span data-ttu-id="4e73a-131">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="4e73a-131">Possible values are:</span></span>
- <span data-ttu-id="4e73a-132">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4e73a-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="4e73a-133">Cena usług zarządzanych wystąpień będzie dyskontowana dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4e73a-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="4e73a-134">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="4e73a-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="4e73a-135">Cena usług zarządzanych wystąpień będzie uwzględniać nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4e73a-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="4e73a-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e73a-136">-Location</span></span>
<span data-ttu-id="4e73a-137">Lokalizacja, w której ma zostać utworzone wystąpienie</span><span class="sxs-lookup"><span data-stu-id="4e73a-137">The location in which to create the instance</span></span>

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

### <span data-ttu-id="4e73a-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e73a-138">-Name</span></span>
<span data-ttu-id="4e73a-139">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4e73a-139">Instance name.</span></span>

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

### <span data-ttu-id="4e73a-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="4e73a-140">-ProxyOverride</span></span>
<span data-ttu-id="4e73a-141">Typ połączenia służący do nawiązywania połączenia z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="4e73a-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="4e73a-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="4e73a-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="4e73a-143">Czy punkt końcowy danych publicznych jest włączony dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4e73a-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="4e73a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e73a-144">-ResourceGroupName</span></span>
<span data-ttu-id="4e73a-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e73a-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73a-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4e73a-146">-SkuName</span></span>
<span data-ttu-id="4e73a-147">Nazwa SKU wystąpienia, na przykład "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="4e73a-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="4e73a-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4e73a-148">-StorageSizeInGB</span></span>
<span data-ttu-id="4e73a-149">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="4e73a-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="4e73a-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4e73a-150">-SubnetId</span></span>
<span data-ttu-id="4e73a-151">Identyfikator podsieci, który ma zostać użyty do utworzenia wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4e73a-151">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="4e73a-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e73a-152">-Tag</span></span>
<span data-ttu-id="4e73a-153">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="4e73a-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="4e73a-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="4e73a-154">-TimezoneId</span></span>
<span data-ttu-id="4e73a-155">Identyfikator strefy czasowej dla wystąpienia, które należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="4e73a-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="4e73a-156">Lista identyfikatorów stref czasowych jest udostępniana za pośrednictwem widoku sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="4e73a-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="4e73a-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="4e73a-157">-VCore</span></span>
<span data-ttu-id="4e73a-158">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="4e73a-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="4e73a-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e73a-159">-Confirm</span></span>
<span data-ttu-id="4e73a-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e73a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e73a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e73a-161">-WhatIf</span></span>
<span data-ttu-id="4e73a-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e73a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e73a-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e73a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e73a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e73a-164">CommonParameters</span></span>
<span data-ttu-id="4e73a-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e73a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e73a-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e73a-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e73a-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e73a-167">INPUTS</span></span>

### <span data-ttu-id="4e73a-168">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4e73a-168">None</span></span>

## <span data-ttu-id="4e73a-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e73a-169">OUTPUTS</span></span>

### <span data-ttu-id="4e73a-170">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4e73a-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="4e73a-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e73a-171">NOTES</span></span>

## <span data-ttu-id="4e73a-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e73a-172">RELATED LINKS</span></span>
