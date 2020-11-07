---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894953"
---
# <span data-ttu-id="8a4d4-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="8a4d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4d4-103">Usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="8a4d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a4d4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a4d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="8a4d4-106">Polecenie cmdlet **Remove-AzSqlDatabase** usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="8a4d4-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8a4d4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a4d4-108">EXAMPLES</span></span>

### <span data-ttu-id="8a4d4-109">Przykład 1: Usuwanie bazy danych z programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a4d4-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8a4d4-110">To polecenie usuwa bazę danych o nazwie Database01 z serwera Server01.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="8a4d4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a4d4-111">PARAMETERS</span></span>

### <span data-ttu-id="8a4d4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a4d4-112">-DatabaseName</span></span>
<span data-ttu-id="8a4d4-113">Określa nazwę bazy danych, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a4d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4d4-114">-DefaultProfile</span></span>
<span data-ttu-id="8a4d4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8a4d4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a4d4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8a4d4-116">-Force</span></span>
<span data-ttu-id="8a4d4-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a4d4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4d4-118">-ResourceGroupName</span></span>
<span data-ttu-id="8a4d4-119">Określa nazwę grupy zasobów platformy Azure, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8a4d4-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8a4d4-120">-ServerName</span></span>
<span data-ttu-id="8a4d4-121">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8a4d4-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a4d4-122">-Confirm</span></span>
<span data-ttu-id="8a4d4-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4d4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4d4-124">-WhatIf</span></span>
<span data-ttu-id="8a4d4-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4d4-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4d4-127">CommonParameters</span></span>
<span data-ttu-id="8a4d4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4d4-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4d4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4d4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a4d4-130">INPUTS</span></span>

### <span data-ttu-id="8a4d4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4d4-131">System.String</span></span>

## <span data-ttu-id="8a4d4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a4d4-132">OUTPUTS</span></span>

### <span data-ttu-id="8a4d4-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8a4d4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8a4d4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a4d4-134">NOTES</span></span>

## <span data-ttu-id="8a4d4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a4d4-135">RELATED LINKS</span></span>

[<span data-ttu-id="8a4d4-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8a4d4-137">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8a4d4-138">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8a4d4-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8a4d4-140">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8a4d4-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8a4d4-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8a4d4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


