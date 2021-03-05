---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 559e23334f9fc98cd51f296aee243152578ba763
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977729"
---
# <span data-ttu-id="d1d73-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d1d73-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d1d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d73-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d73-103">Tworzy bazę danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="d1d73-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d1d73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1d73-104">SYNTAX</span></span>

### <span data-ttu-id="d1d73-105">CreateNewInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d1d73-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d73-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d1d73-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d73-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d73-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1d73-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1d73-108">DESCRIPTION</span></span>
<span data-ttu-id="d1d73-109">Polecenie **cmdlet New-AzSqlInstanceDatabase** tworzy bazę danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="d1d73-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="d1d73-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1d73-110">EXAMPLES</span></span>

### <span data-ttu-id="d1d73-111">Przykład 1. Tworzenie bazy danych w określonym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="d1d73-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="d1d73-112">To polecenie tworzy wystąpienie bazy danych o nazwie Database01 w wystąpieniu managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="d1d73-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="d1d73-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d73-113">PARAMETERS</span></span>

### <span data-ttu-id="d1d73-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d1d73-114">-AsJob</span></span>
<span data-ttu-id="d1d73-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d1d73-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1d73-116">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="d1d73-116">-Collation</span></span>
<span data-ttu-id="d1d73-117">Sortowanie danych usługi Azure SQL Instance Database do użycia.</span><span class="sxs-lookup"><span data-stu-id="d1d73-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="d1d73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d73-118">-DefaultProfile</span></span>
<span data-ttu-id="d1d73-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d73-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d73-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1d73-120">-InstanceName</span></span>
<span data-ttu-id="d1d73-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d1d73-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d73-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="d1d73-122">-InstanceObject</span></span>
<span data-ttu-id="d1d73-123">Obiekt wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d1d73-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d73-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d73-124">-InstanceResourceId</span></span>
<span data-ttu-id="d1d73-125">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d1d73-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d73-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1d73-126">-Name</span></span>
<span data-ttu-id="d1d73-127">Nazwa bazy danych Azure SQL Instance Database do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d1d73-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d73-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1d73-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1d73-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d73-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="d1d73-130">-Tag</span></span>
<span data-ttu-id="d1d73-131">Tagi do skojarzenia z bazą danych Azure Sql Instance Database</span><span class="sxs-lookup"><span data-stu-id="d1d73-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="d1d73-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1d73-132">-Confirm</span></span>
<span data-ttu-id="d1d73-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1d73-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d73-134">-WhatIf</span></span>
<span data-ttu-id="d1d73-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d73-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d73-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1d73-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d73-137">CommonParameters</span></span>
<span data-ttu-id="d1d73-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d73-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1d73-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d73-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1d73-140">INPUTS</span></span>

### <span data-ttu-id="d1d73-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d1d73-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d1d73-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d73-142">System.String</span></span>

## <span data-ttu-id="d1d73-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1d73-143">OUTPUTS</span></span>

### <span data-ttu-id="d1d73-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d1d73-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d1d73-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1d73-145">NOTES</span></span>

## <span data-ttu-id="d1d73-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1d73-146">RELATED LINKS</span></span>
