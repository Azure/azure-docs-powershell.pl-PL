---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9688475a1d8bae19b10bc5626dca643ac947156d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961409"
---
# <span data-ttu-id="34783-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="34783-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="34783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34783-102">SYNOPSIS</span></span>
<span data-ttu-id="34783-103">Usuwa ustawienia inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="34783-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="34783-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34783-104">SYNTAX</span></span>

### <span data-ttu-id="34783-105">DatabaseParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="34783-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34783-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34783-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34783-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34783-107">DESCRIPTION</span></span>
<span data-ttu-id="34783-108">Polecenie **cmdlet Remove-AzSqlDatabaseAudit** usuwa ustawienia inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="34783-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="34783-109">Aby użyć polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="34783-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="34783-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34783-110">EXAMPLES</span></span>

### <span data-ttu-id="34783-111">Przykład 1. Usuwanie ustawień inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="34783-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="34783-112">Przykład 2. Usuwanie ustawień inspekcji bazy danych Azure SQL za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="34783-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="34783-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34783-113">PARAMETERS</span></span>

### <span data-ttu-id="34783-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34783-114">-DatabaseName</span></span>
<span data-ttu-id="34783-115">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34783-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34783-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="34783-116">-DatabaseObject</span></span>
<span data-ttu-id="34783-117">Obiekt bazy danych do zarządzania jego zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="34783-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34783-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34783-118">-DefaultProfile</span></span>
<span data-ttu-id="34783-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34783-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34783-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34783-120">-ResourceGroupName</span></span>
<span data-ttu-id="34783-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34783-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34783-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34783-122">-ServerName</span></span>
<span data-ttu-id="34783-123">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="34783-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34783-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34783-124">-Confirm</span></span>
<span data-ttu-id="34783-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34783-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34783-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34783-126">-WhatIf</span></span>
<span data-ttu-id="34783-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34783-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34783-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34783-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34783-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34783-129">CommonParameters</span></span>
<span data-ttu-id="34783-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34783-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34783-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34783-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34783-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34783-132">INPUTS</span></span>

### <span data-ttu-id="34783-133">System.String</span><span class="sxs-lookup"><span data-stu-id="34783-133">System.String</span></span>

### <span data-ttu-id="34783-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="34783-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="34783-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34783-135">OUTPUTS</span></span>

### <span data-ttu-id="34783-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34783-136">System.Boolean</span></span>

## <span data-ttu-id="34783-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34783-137">NOTES</span></span>

## <span data-ttu-id="34783-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34783-138">RELATED LINKS</span></span>
