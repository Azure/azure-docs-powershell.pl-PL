---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551104"
---
# <span data-ttu-id="dd543-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd543-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="dd543-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd543-102">SYNOPSIS</span></span>
<span data-ttu-id="dd543-103">Ustawia właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dd543-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd543-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd543-104">SYNTAX</span></span>

### <span data-ttu-id="dd543-105">SetInstanceFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd543-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd543-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="dd543-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd543-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="dd543-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd543-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dd543-108">DESCRIPTION</span></span>
<span data-ttu-id="dd543-109">Polecenie cmdlet **Set-AzureRmSqlInstance** modyfikuje właściwości wystąpienia zarządzanego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dd543-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="dd543-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd543-110">EXAMPLES</span></span>

### <span data-ttu-id="dd543-111">Przykład 1: Ustawianie istniejącego wystąpienia przy użyciu nowych wartości dla-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="dd543-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="dd543-112">To polecenie ustawia istniejące wystąpienie przy użyciu nowych wartości-AdministratorPassword,-LicenseType,-StorageSizeInGB i-VCore</span><span class="sxs-lookup"><span data-stu-id="dd543-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="dd543-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd543-113">PARAMETERS</span></span>

### <span data-ttu-id="dd543-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="dd543-114">-AdministratorPassword</span></span>
<span data-ttu-id="dd543-115">Nowe hasło administratora SQL dla wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dd543-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dd543-116">-AssignIdentity</span></span>
<span data-ttu-id="dd543-117">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego wystąpienia, aby móc korzystać z usług zarządzania kluczami, takich jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dd543-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="dd543-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd543-118">-DefaultProfile</span></span>
<span data-ttu-id="dd543-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd543-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd543-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="dd543-120">-Edition</span></span>
<span data-ttu-id="dd543-121">Wersja do przypisania do wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dd543-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dd543-122">-Force</span></span>
<span data-ttu-id="dd543-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="dd543-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dd543-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd543-124">-InputObject</span></span>
<span data-ttu-id="dd543-125">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="dd543-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dd543-126">-LicenseType</span></span>
<span data-ttu-id="dd543-127">Określa typ licencji, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="dd543-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd543-128">-Name</span></span>
<span data-ttu-id="dd543-129">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="dd543-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd543-130">-ResourceGroupName</span></span>
<span data-ttu-id="dd543-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd543-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd543-132">-ResourceId</span></span>
<span data-ttu-id="dd543-133">Identyfikator zasobu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="dd543-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dd543-134">-StorageSizeInGB</span></span>
<span data-ttu-id="dd543-135">Określa ilość miejsca do magazynowania, które ma zostać skojarzone z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="dd543-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd543-136">-Tag</span></span>
<span data-ttu-id="dd543-137">Znaczniki, które mają zostać skojarzone z instancją.</span><span class="sxs-lookup"><span data-stu-id="dd543-137">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="dd543-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="dd543-138">-VCore</span></span>
<span data-ttu-id="dd543-139">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="dd543-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd543-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd543-140">-Confirm</span></span>
<span data-ttu-id="dd543-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd543-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd543-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd543-142">-WhatIf</span></span>
<span data-ttu-id="dd543-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd543-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd543-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd543-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd543-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd543-145">CommonParameters</span></span>
<span data-ttu-id="dd543-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd543-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd543-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd543-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd543-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd543-148">INPUTS</span></span>

### <span data-ttu-id="dd543-149">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="dd543-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="dd543-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dd543-150">System.String</span></span>

## <span data-ttu-id="dd543-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd543-151">OUTPUTS</span></span>

### <span data-ttu-id="dd543-152">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="dd543-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="dd543-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd543-153">NOTES</span></span>

## <span data-ttu-id="dd543-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd543-154">RELATED LINKS</span></span>
