---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: 342944fbd933f135f3643d4022f965405de2f1df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707810"
---
# <span data-ttu-id="d33b7-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d33b7-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d33b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d33b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d33b7-103">Usuwa bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d33b7-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d33b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d33b7-104">SYNTAX</span></span>

### <span data-ttu-id="d33b7-105">RemoveInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d33b7-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d33b7-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d33b7-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d33b7-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d33b7-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33b7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d33b7-108">DESCRIPTION</span></span>
<span data-ttu-id="d33b7-109">Polecenie cmdlet **Remove-AzSqlInstanceDatabase** usuwa bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d33b7-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d33b7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d33b7-110">EXAMPLES</span></span>

### <span data-ttu-id="d33b7-111">Przykład 1: Usuwanie bazy danych z wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d33b7-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d33b7-112">To polecenie usuwa bazę danych o nazwie Database01 z wystąpienia managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="d33b7-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="d33b7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d33b7-113">PARAMETERS</span></span>

### <span data-ttu-id="d33b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33b7-114">-DefaultProfile</span></span>
<span data-ttu-id="d33b7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d33b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d33b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d33b7-116">-Force</span></span>
<span data-ttu-id="d33b7-117">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="d33b7-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d33b7-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d33b7-118">-InputObject</span></span>
<span data-ttu-id="d33b7-119">Obiekt bazy danych wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d33b7-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="d33b7-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d33b7-120">-InstanceName</span></span>
<span data-ttu-id="d33b7-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d33b7-121">The instance name.</span></span>

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

### <span data-ttu-id="d33b7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d33b7-122">-Name</span></span>
<span data-ttu-id="d33b7-123">Nazwa bazy danych wystąpienia SQL Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d33b7-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="d33b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d33b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d33b7-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d33b7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d33b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d33b7-126">-ResourceId</span></span>
<span data-ttu-id="d33b7-127">Identyfikator zasobu wystąpienia obiektu bazy danych do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d33b7-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="d33b7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d33b7-128">-Confirm</span></span>
<span data-ttu-id="d33b7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d33b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d33b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33b7-130">-WhatIf</span></span>
<span data-ttu-id="d33b7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d33b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d33b7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d33b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d33b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33b7-133">CommonParameters</span></span>
<span data-ttu-id="d33b7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33b7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d33b7-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33b7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d33b7-136">INPUTS</span></span>

### <span data-ttu-id="d33b7-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d33b7-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="d33b7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d33b7-138">System.String</span></span>

## <span data-ttu-id="d33b7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d33b7-139">OUTPUTS</span></span>

### <span data-ttu-id="d33b7-140">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d33b7-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d33b7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d33b7-141">NOTES</span></span>

## <span data-ttu-id="d33b7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d33b7-142">RELATED LINKS</span></span>