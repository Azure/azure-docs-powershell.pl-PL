---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546399"
---
# <span data-ttu-id="91412-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="91412-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91412-102">SYNOPSIS</span></span>
<span data-ttu-id="91412-103">Wznawia bazę danych hurtowni danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91412-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91412-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91412-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91412-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91412-105">DESCRIPTION</span></span>
<span data-ttu-id="91412-106">Polecenie cmdlet **Resume-AzureRmSqlDatabase** wznawia bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91412-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="91412-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91412-107">EXAMPLES</span></span>

### <span data-ttu-id="91412-108">Przykład 1: wznawia bazę danych hurtowni danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="91412-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="91412-109">To polecenie wznawia wstrzymaną bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91412-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="91412-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91412-110">PARAMETERS</span></span>

### <span data-ttu-id="91412-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91412-111">-AsJob</span></span>
<span data-ttu-id="91412-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91412-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91412-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91412-113">-DatabaseName</span></span>
<span data-ttu-id="91412-114">Określa nazwę bazy danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91412-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="91412-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91412-115">-DefaultProfile</span></span>
<span data-ttu-id="91412-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="91412-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91412-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91412-117">-ResourceGroupName</span></span>
<span data-ttu-id="91412-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="91412-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="91412-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="91412-119">-ServerName</span></span>
<span data-ttu-id="91412-120">Określa nazwę serwera obsługującego bazę danych, która zostanie wznowiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91412-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="91412-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91412-121">-Confirm</span></span>
<span data-ttu-id="91412-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91412-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91412-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91412-123">-WhatIf</span></span>
<span data-ttu-id="91412-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91412-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91412-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91412-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91412-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91412-126">CommonParameters</span></span>
<span data-ttu-id="91412-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91412-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91412-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91412-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91412-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91412-129">INPUTS</span></span>

### <span data-ttu-id="91412-130">System. String</span><span class="sxs-lookup"><span data-stu-id="91412-130">System.String</span></span>

## <span data-ttu-id="91412-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91412-131">OUTPUTS</span></span>

### <span data-ttu-id="91412-132">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="91412-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="91412-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91412-133">NOTES</span></span>
* <span data-ttu-id="91412-134">Polecenie cmdlet **Resume-AzureRmSqlDatabase** działa tylko w przypadku baz danych hurtowni danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91412-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="91412-135">Ta operacja nie jest obsługiwana w przypadku usługi Azure SQL Database Basic, wersji Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="91412-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="91412-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91412-136">RELATED LINKS</span></span>

[<span data-ttu-id="91412-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="91412-138">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="91412-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="91412-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="91412-141">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91412-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="91412-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="91412-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


