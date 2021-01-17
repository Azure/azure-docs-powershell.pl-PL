---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376490"
---
# <span data-ttu-id="43714-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="43714-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43714-102">SYNOPSIS</span></span>
<span data-ttu-id="43714-103">Wznawia bazę danych hurtowni danych SQL.</span><span class="sxs-lookup"><span data-stu-id="43714-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="43714-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43714-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43714-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43714-105">DESCRIPTION</span></span>
<span data-ttu-id="43714-106">Polecenie cmdlet **Resume-AzSqlDatabase** wznawia bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="43714-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="43714-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43714-107">EXAMPLES</span></span>

### <span data-ttu-id="43714-108">Przykład 1: wznawia bazę danych hurtowni danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="43714-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="43714-109">To polecenie wznawia wstrzymaną bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="43714-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="43714-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43714-110">PARAMETERS</span></span>

### <span data-ttu-id="43714-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43714-111">-AsJob</span></span>
<span data-ttu-id="43714-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="43714-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43714-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43714-113">-DatabaseName</span></span>
<span data-ttu-id="43714-114">Określa nazwę bazy danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43714-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="43714-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43714-115">-DefaultProfile</span></span>
<span data-ttu-id="43714-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="43714-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43714-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43714-117">-ResourceGroupName</span></span>
<span data-ttu-id="43714-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="43714-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="43714-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="43714-119">-ServerName</span></span>
<span data-ttu-id="43714-120">Określa nazwę serwera obsługującego bazę danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43714-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="43714-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43714-121">-Confirm</span></span>
<span data-ttu-id="43714-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43714-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43714-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43714-123">-WhatIf</span></span>
<span data-ttu-id="43714-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43714-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43714-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43714-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43714-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43714-126">CommonParameters</span></span>
<span data-ttu-id="43714-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43714-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43714-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43714-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43714-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43714-129">INPUTS</span></span>

### <span data-ttu-id="43714-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43714-130">System.String</span></span>

## <span data-ttu-id="43714-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43714-131">OUTPUTS</span></span>

### <span data-ttu-id="43714-132">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="43714-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="43714-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43714-133">NOTES</span></span>
* <span data-ttu-id="43714-134">Polecenie cmdlet **Resume-AzSqlDatabase** działa tylko w przypadku baz danych hurtowni danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="43714-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="43714-135">Ta operacja nie jest obsługiwana w przypadku usługi Azure SQL Database Basic, wersji Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="43714-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="43714-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43714-136">RELATED LINKS</span></span>

[<span data-ttu-id="43714-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="43714-138">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="43714-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="43714-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="43714-141">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43714-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="43714-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="43714-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


