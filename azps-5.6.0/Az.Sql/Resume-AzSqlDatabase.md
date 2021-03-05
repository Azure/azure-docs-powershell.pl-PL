---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: 3ba3703882371975ee9b0d2f87bd03b75b58e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995037"
---
# <span data-ttu-id="48085-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="48085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48085-102">SYNOPSIS</span></span>
<span data-ttu-id="48085-103">Wznawia pracę z bazą danych programu SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="48085-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="48085-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48085-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48085-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="48085-105">DESCRIPTION</span></span>
<span data-ttu-id="48085-106">Polecenie cmdlet **Resume-AzSqlDatabase** wznawia bazę danych usługi Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="48085-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="48085-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48085-107">EXAMPLES</span></span>

### <span data-ttu-id="48085-108">Przykład 1. Wznawia korzystanie z bazy danych azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="48085-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="48085-109">To polecenie wznawia zawieszoną bazę danych usługi Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="48085-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="48085-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48085-110">PARAMETERS</span></span>

### <span data-ttu-id="48085-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="48085-111">-AsJob</span></span>
<span data-ttu-id="48085-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="48085-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48085-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48085-113">-DatabaseName</span></span>
<span data-ttu-id="48085-114">Określa nazwę bazy danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48085-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="48085-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48085-115">-DefaultProfile</span></span>
<span data-ttu-id="48085-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="48085-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48085-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48085-117">-ResourceGroupName</span></span>
<span data-ttu-id="48085-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="48085-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="48085-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48085-119">-ServerName</span></span>
<span data-ttu-id="48085-120">Określa nazwę serwera hostowego bazę danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48085-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="48085-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48085-121">-Confirm</span></span>
<span data-ttu-id="48085-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48085-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48085-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48085-123">-WhatIf</span></span>
<span data-ttu-id="48085-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48085-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48085-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48085-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48085-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48085-126">CommonParameters</span></span>
<span data-ttu-id="48085-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48085-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48085-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48085-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48085-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48085-129">INPUTS</span></span>

### <span data-ttu-id="48085-130">System.String</span><span class="sxs-lookup"><span data-stu-id="48085-130">System.String</span></span>

## <span data-ttu-id="48085-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48085-131">OUTPUTS</span></span>

### <span data-ttu-id="48085-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="48085-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="48085-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48085-133">NOTES</span></span>
* <span data-ttu-id="48085-134">Polecenie **cmdlet Resume-AzSqlDatabase** działa tylko w bazach danych programu Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="48085-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="48085-135">Ta operacja nie jest obsługiwana w przypadku wersji Azure SQL Database Basic, Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="48085-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="48085-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48085-136">RELATED LINKS</span></span>

[<span data-ttu-id="48085-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="48085-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="48085-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="48085-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="48085-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48085-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="48085-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="48085-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


