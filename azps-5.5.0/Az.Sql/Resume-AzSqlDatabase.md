---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201410"
---
# <span data-ttu-id="a67f5-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="a67f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a67f5-103">Wznawia pracę z bazą danych programu SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="a67f5-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a67f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a67f5-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67f5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a67f5-105">DESCRIPTION</span></span>
<span data-ttu-id="a67f5-106">Polecenie cmdlet **Resume-AzSqlDatabase** wznawia bazę danych usługi Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="a67f5-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a67f5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a67f5-107">EXAMPLES</span></span>

### <span data-ttu-id="a67f5-108">Przykład 1. Wznawia korzystanie z bazy danych azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="a67f5-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a67f5-109">To polecenie wznawia zawieszoną bazę danych usługi Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="a67f5-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a67f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67f5-110">PARAMETERS</span></span>

### <span data-ttu-id="a67f5-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a67f5-111">-AsJob</span></span>
<span data-ttu-id="a67f5-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a67f5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a67f5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a67f5-113">-DatabaseName</span></span>
<span data-ttu-id="a67f5-114">Określa nazwę bazy danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67f5-114">Specifies the name of the database that this cmdlet resumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67f5-115">-DefaultProfile</span></span>
<span data-ttu-id="a67f5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a67f5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a67f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a67f5-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="a67f5-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a67f5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a67f5-119">-ServerName</span></span>
<span data-ttu-id="a67f5-120">Określa nazwę serwera hostowego bazę danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67f5-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a67f5-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a67f5-121">-Confirm</span></span>
<span data-ttu-id="a67f5-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a67f5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67f5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67f5-123">-WhatIf</span></span>
<span data-ttu-id="a67f5-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67f5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67f5-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a67f5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67f5-126">CommonParameters</span></span>
<span data-ttu-id="a67f5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67f5-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a67f5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67f5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67f5-129">INPUTS</span></span>

### <span data-ttu-id="a67f5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a67f5-130">System.String</span></span>

## <span data-ttu-id="a67f5-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67f5-131">OUTPUTS</span></span>

### <span data-ttu-id="a67f5-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a67f5-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a67f5-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a67f5-133">NOTES</span></span>
* <span data-ttu-id="a67f5-134">Polecenie **cmdlet Resume-AzSqlDatabase** działa tylko w bazach danych programu Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="a67f5-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a67f5-135">Ta operacja nie jest obsługiwana w przypadku wersji Azure SQL Database Basic, Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a67f5-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a67f5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a67f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a67f5-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a67f5-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="a67f5-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="a67f5-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="a67f5-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a67f5-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="a67f5-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a67f5-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


