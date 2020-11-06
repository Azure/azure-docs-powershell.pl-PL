---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546408"
---
# <span data-ttu-id="4273e-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4273e-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="4273e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4273e-102">SYNOPSIS</span></span>
<span data-ttu-id="4273e-103">Tworzy bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4273e-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4273e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4273e-104">SYNTAX</span></span>

### <span data-ttu-id="4273e-105">CreateNewInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4273e-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4273e-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4273e-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4273e-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="4273e-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4273e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4273e-108">DESCRIPTION</span></span>
<span data-ttu-id="4273e-109">Polecenie cmdlet **New-AzureRmSqlInstanceDatabase** tworzy bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4273e-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="4273e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4273e-110">EXAMPLES</span></span>

### <span data-ttu-id="4273e-111">Przykład 1: Tworzenie bazy danych w określonym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="4273e-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="4273e-112">To polecenie tworzy bazę danych wystąpienia o nazwie Database01 w wystąpieniu managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="4273e-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="4273e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4273e-113">PARAMETERS</span></span>

### <span data-ttu-id="4273e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4273e-114">-AsJob</span></span>
<span data-ttu-id="4273e-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4273e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4273e-116">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="4273e-116">-Collation</span></span>
<span data-ttu-id="4273e-117">Sortowanie sortowania bazy danych wystąpienia SQL Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="4273e-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="4273e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4273e-118">-DefaultProfile</span></span>
<span data-ttu-id="4273e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4273e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4273e-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4273e-120">-InstanceName</span></span>
<span data-ttu-id="4273e-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="4273e-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4273e-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="4273e-122">-InstanceObject</span></span>
<span data-ttu-id="4273e-123">Obiekt wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4273e-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4273e-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="4273e-124">-InstanceResourceId</span></span>
<span data-ttu-id="4273e-125">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4273e-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4273e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4273e-126">-Name</span></span>
<span data-ttu-id="4273e-127">Nazwa bazy danych wystąpienia SQL Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4273e-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4273e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4273e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4273e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4273e-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4273e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4273e-130">-Tag</span></span>
<span data-ttu-id="4273e-131">Tagi, które mają zostać skojarzone z bazą danych wystąpienia SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4273e-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="4273e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4273e-132">-Confirm</span></span>
<span data-ttu-id="4273e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4273e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4273e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4273e-134">-WhatIf</span></span>
<span data-ttu-id="4273e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4273e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4273e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4273e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4273e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4273e-137">CommonParameters</span></span>
<span data-ttu-id="4273e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4273e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4273e-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4273e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4273e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4273e-140">INPUTS</span></span>

### <span data-ttu-id="4273e-141">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4273e-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="4273e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4273e-142">System.String</span></span>

## <span data-ttu-id="4273e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4273e-143">OUTPUTS</span></span>

### <span data-ttu-id="4273e-144">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4273e-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="4273e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4273e-145">NOTES</span></span>

## <span data-ttu-id="4273e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4273e-146">RELATED LINKS</span></span>
