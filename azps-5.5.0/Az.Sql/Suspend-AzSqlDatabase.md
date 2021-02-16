---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195898"
---
# <span data-ttu-id="46a24-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="46a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a24-102">SYNOPSIS</span></span>
<span data-ttu-id="46a24-103">Zawiesza bazę danych programu SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="46a24-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="46a24-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46a24-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a24-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46a24-105">DESCRIPTION</span></span>
<span data-ttu-id="46a24-106">Polecenie cmdlet **Suspend-AzSqlDatabase** zawiesza bazę danych programu Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="46a24-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="46a24-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46a24-107">EXAMPLES</span></span>

### <span data-ttu-id="46a24-108">Przykład 1. Zawiesza bazę danych usługi Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="46a24-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="46a24-109">To polecenie powoduje zawieszenie aktywnej bazy danych programu Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="46a24-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="46a24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a24-110">PARAMETERS</span></span>

### <span data-ttu-id="46a24-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="46a24-111">-AsJob</span></span>
<span data-ttu-id="46a24-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="46a24-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46a24-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46a24-113">-DatabaseName</span></span>
<span data-ttu-id="46a24-114">Określa nazwę bazy danych, która jest zawieszana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46a24-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="46a24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a24-115">-DefaultProfile</span></span>
<span data-ttu-id="46a24-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="46a24-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46a24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a24-117">-ResourceGroupName</span></span>
<span data-ttu-id="46a24-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="46a24-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="46a24-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46a24-119">-ServerName</span></span>
<span data-ttu-id="46a24-120">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="46a24-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="46a24-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46a24-121">-Confirm</span></span>
<span data-ttu-id="46a24-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46a24-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a24-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a24-123">-WhatIf</span></span>
<span data-ttu-id="46a24-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46a24-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a24-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="46a24-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a24-126">CommonParameters</span></span>
<span data-ttu-id="46a24-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a24-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46a24-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a24-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46a24-129">INPUTS</span></span>

### <span data-ttu-id="46a24-130">System.String</span><span class="sxs-lookup"><span data-stu-id="46a24-130">System.String</span></span>

## <span data-ttu-id="46a24-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46a24-131">OUTPUTS</span></span>

### <span data-ttu-id="46a24-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="46a24-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="46a24-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46a24-133">NOTES</span></span>
* <span data-ttu-id="46a24-134">Polecenie cmdlet **Suspend-AzSqlDatabase** działa tylko w bazach danych programu Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="46a24-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="46a24-135">Ta operacja nie jest obsługiwana w przypadku wersji Azure SQL Database Basic, Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="46a24-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="46a24-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46a24-136">RELATED LINKS</span></span>

[<span data-ttu-id="46a24-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="46a24-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="46a24-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="46a24-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="46a24-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a24-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="46a24-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="46a24-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


