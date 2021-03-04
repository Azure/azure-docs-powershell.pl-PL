---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: 5b1817ef0924f4e7bb1c07152b9adc47cc27292f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955137"
---
# <span data-ttu-id="a4543-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a4543-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="a4543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4543-102">SYNOPSIS</span></span>
<span data-ttu-id="a4543-103">Usuwa bazę danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="a4543-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a4543-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4543-104">SYNTAX</span></span>

### <span data-ttu-id="a4543-105">RemoveInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4543-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4543-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a4543-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4543-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a4543-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4543-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4543-108">DESCRIPTION</span></span>
<span data-ttu-id="a4543-109">Polecenie **cmdlet Remove-AzSqlInstanceDatabase** usuwa bazę danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="a4543-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a4543-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4543-110">EXAMPLES</span></span>

### <span data-ttu-id="a4543-111">Przykład 1. Usuwanie bazy danych z wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a4543-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4543-112">To polecenie usuwa bazę danych o nazwie Database01 z wystąpienia managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a4543-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="a4543-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4543-113">PARAMETERS</span></span>

### <span data-ttu-id="a4543-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4543-114">-DefaultProfile</span></span>
<span data-ttu-id="a4543-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4543-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4543-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a4543-116">-Force</span></span>
<span data-ttu-id="a4543-117">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="a4543-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a4543-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4543-118">-InputObject</span></span>
<span data-ttu-id="a4543-119">Obiekt Instance Database do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a4543-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4543-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a4543-120">-InstanceName</span></span>
<span data-ttu-id="a4543-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a4543-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4543-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4543-122">-Name</span></span>
<span data-ttu-id="a4543-123">Nazwa bazy danych Azure SQL Instance Database do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a4543-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4543-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4543-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4543-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4543-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4543-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4543-126">-ResourceId</span></span>
<span data-ttu-id="a4543-127">Identyfikator zasobu obiektu instance database do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a4543-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4543-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4543-128">-Confirm</span></span>
<span data-ttu-id="a4543-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4543-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4543-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4543-130">-WhatIf</span></span>
<span data-ttu-id="a4543-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4543-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4543-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4543-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4543-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4543-133">CommonParameters</span></span>
<span data-ttu-id="a4543-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4543-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4543-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4543-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4543-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4543-136">INPUTS</span></span>

### <span data-ttu-id="a4543-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4543-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="a4543-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a4543-138">System.String</span></span>

## <span data-ttu-id="a4543-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4543-139">OUTPUTS</span></span>

### <span data-ttu-id="a4543-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4543-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a4543-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4543-141">NOTES</span></span>

## <span data-ttu-id="a4543-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4543-142">RELATED LINKS</span></span>
