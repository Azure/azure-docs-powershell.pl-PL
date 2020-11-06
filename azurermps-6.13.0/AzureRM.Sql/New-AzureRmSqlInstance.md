---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553440"
---
# <span data-ttu-id="5d3c2-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3c2-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="5d3c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3c2-103">Tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d3c2-104">SYNTAX</span></span>

### <span data-ttu-id="5d3c2-105">NewByEditionAndComputeGenerationParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d3c2-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3c2-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="5d3c2-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3c2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d3c2-107">DESCRIPTION</span></span>
<span data-ttu-id="5d3c2-108">Polecenie cmdlet **New-AzureRmSqlInstance** tworzy wystąpienie zarządzane bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="5d3c2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d3c2-109">EXAMPLES</span></span>

### <span data-ttu-id="5d3c2-110">Przykład 1. Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="5d3c2-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="5d3c2-111">To polecenie tworzy nowe wystąpienie przy użyciu parametrów wersja i ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="5d3c2-112">Przykład 2: Tworzenie nowego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="5d3c2-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="5d3c2-113">To polecenie tworzy nowe wystąpienie za pomocą parametrów wersja i ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="5d3c2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d3c2-114">PARAMETERS</span></span>

### <span data-ttu-id="5d3c2-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="5d3c2-115">-AdministratorCredential</span></span>
<span data-ttu-id="5d3c2-116">Poświadczenie uwierzytelniania SQL wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d3c2-117">-AsJob</span></span>
<span data-ttu-id="5d3c2-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5d3c2-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5d3c2-119">-AssignIdentity</span></span>
<span data-ttu-id="5d3c2-120">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia zarządzanego, które ma być używane z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5d3c2-121">-ComputeGeneration</span></span>
<span data-ttu-id="5d3c2-122">Generowanie obliczeń dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3c2-123">-DefaultProfile</span></span>
<span data-ttu-id="5d3c2-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="5d3c2-125">-Edition</span></span>
<span data-ttu-id="5d3c2-126">Wersja dla tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d3c2-127">-LicenseType</span></span>
<span data-ttu-id="5d3c2-128">Określa typ licencji, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="5d3c2-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5d3c2-129">-Location</span></span>
<span data-ttu-id="5d3c2-130">Lokalizacja, w której ma zostać utworzone wystąpienie</span><span class="sxs-lookup"><span data-stu-id="5d3c2-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d3c2-131">-Name</span></span>
<span data-ttu-id="5d3c2-132">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-133">-ResourceGroupName</span></span>
<span data-ttu-id="5d3c2-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-135">-SkuName</span></span>
<span data-ttu-id="5d3c2-136">Nazwa SKU wystąpienia, na przykład "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="5d3c2-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5d3c2-137">-StorageSizeInGB</span></span>
<span data-ttu-id="5d3c2-138">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5d3c2-139">-SubnetId</span></span>
<span data-ttu-id="5d3c2-140">Identyfikator podsieci, który ma zostać użyty do utworzenia wystąpienia</span><span class="sxs-lookup"><span data-stu-id="5d3c2-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d3c2-141">-Tag</span></span>
<span data-ttu-id="5d3c2-142">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="5d3c2-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="5d3c2-143">-VCore</span></span>
<span data-ttu-id="5d3c2-144">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d3c2-145">-Confirm</span></span>
<span data-ttu-id="5d3c2-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3c2-147">-WhatIf</span></span>
<span data-ttu-id="5d3c2-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3c2-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3c2-150">CommonParameters</span></span>
<span data-ttu-id="5d3c2-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3c2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3c2-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3c2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3c2-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d3c2-153">INPUTS</span></span>

### <span data-ttu-id="5d3c2-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5d3c2-154">None</span></span>

## <span data-ttu-id="5d3c2-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d3c2-155">OUTPUTS</span></span>

### <span data-ttu-id="5d3c2-156">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5d3c2-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="5d3c2-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d3c2-157">NOTES</span></span>

## <span data-ttu-id="5d3c2-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d3c2-158">RELATED LINKS</span></span>
