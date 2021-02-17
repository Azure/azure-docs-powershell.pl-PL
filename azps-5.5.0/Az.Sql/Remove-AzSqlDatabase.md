---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196074"
---
# <span data-ttu-id="0bd81-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="0bd81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd81-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd81-103">Usuwa bazę danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0bd81-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="0bd81-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bd81-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd81-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bd81-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd81-106">Polecenie **cmdlet Remove-AzSqlDatabase** usuwa bazę danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0bd81-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="0bd81-107">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd81-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0bd81-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bd81-108">EXAMPLES</span></span>

### <span data-ttu-id="0bd81-109">Przykład 1. Usuwanie bazy danych z serwera Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="0bd81-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0bd81-110">To polecenie usuwa bazę danych o nazwie Database01 z serwera Server01.</span><span class="sxs-lookup"><span data-stu-id="0bd81-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="0bd81-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bd81-111">PARAMETERS</span></span>

### <span data-ttu-id="0bd81-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0bd81-112">-DatabaseName</span></span>
<span data-ttu-id="0bd81-113">Określa nazwę bazy danych, która zostanie usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bd81-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd81-114">-DefaultProfile</span></span>
<span data-ttu-id="0bd81-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0bd81-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bd81-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0bd81-116">-Force</span></span>
<span data-ttu-id="0bd81-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0bd81-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0bd81-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd81-118">-ResourceGroupName</span></span>
<span data-ttu-id="0bd81-119">Określa nazwę grupy zasobów platformy Azure, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="0bd81-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd81-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0bd81-120">-ServerName</span></span>
<span data-ttu-id="0bd81-121">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="0bd81-121">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd81-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bd81-122">-Confirm</span></span>
<span data-ttu-id="0bd81-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0bd81-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bd81-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd81-124">-WhatIf</span></span>
<span data-ttu-id="0bd81-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bd81-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd81-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0bd81-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bd81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd81-127">CommonParameters</span></span>
<span data-ttu-id="0bd81-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd81-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bd81-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd81-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bd81-130">INPUTS</span></span>

### <span data-ttu-id="0bd81-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0bd81-131">System.String</span></span>

## <span data-ttu-id="0bd81-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bd81-132">OUTPUTS</span></span>

### <span data-ttu-id="0bd81-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0bd81-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0bd81-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bd81-134">NOTES</span></span>

## <span data-ttu-id="0bd81-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bd81-135">RELATED LINKS</span></span>

[<span data-ttu-id="0bd81-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0bd81-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="0bd81-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0bd81-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0bd81-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd81-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="0bd81-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0bd81-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


