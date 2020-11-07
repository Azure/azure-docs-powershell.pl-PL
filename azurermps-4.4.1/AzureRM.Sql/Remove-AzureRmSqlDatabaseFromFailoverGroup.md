---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: b796d1247d1f8a49316431ca944ac6cd1fb77d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719520"
---
# <span data-ttu-id="88ed6-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="88ed6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="88ed6-103">Usuwa co najmniej jeden z baz danych z grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ed6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88ed6-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88ed6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="88ed6-106">Usuwa co najmniej jeden z baz danych z określonej grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="88ed6-107">Bazy danych i relacje replikacji pozostają nienaruszone, ale nie będą już dostępne w punktach końcowych grup pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="88ed6-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="88ed6-108">Aby uzyskać obiekty bazy danych, do których ma zostać wypełniony parametr "-Database", użyj (na przykład) polecenia cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="88ed6-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="88ed6-109">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="88ed6-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="88ed6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88ed6-110">EXAMPLES</span></span>

### <span data-ttu-id="88ed6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88ed6-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="88ed6-112">To polecenie umożliwia usunięcie jednej bazy danych z grupy trybu failover przez przejście do niej.</span><span class="sxs-lookup"><span data-stu-id="88ed6-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="88ed6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88ed6-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="88ed6-114">To polecenie usuwa wszystkie bazy danych z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="88ed6-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="88ed6-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="88ed6-116">To polecenie usuwa wszystkie bazy danych z grupy elastycznej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="88ed6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88ed6-117">PARAMETERS</span></span>

### <span data-ttu-id="88ed6-118">-Database</span><span class="sxs-lookup"><span data-stu-id="88ed6-118">-Database</span></span>
<span data-ttu-id="88ed6-119">Co najmniej jedna baza danych SQL Azure na serwerze podstawowym grupy trybu failover do usunięcia z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ed6-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="88ed6-120">-FailoverGroupName</span></span>
<span data-ttu-id="88ed6-121">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="88ed6-121">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ed6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="88ed6-122">-Force</span></span>
<span data-ttu-id="88ed6-123">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="88ed6-123">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="88ed6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ed6-124">-ResourceGroupName</span></span>
<span data-ttu-id="88ed6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88ed6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="88ed6-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="88ed6-126">-ServerName</span></span>
<span data-ttu-id="88ed6-127">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="88ed6-127">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="88ed6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88ed6-128">-Confirm</span></span>
<span data-ttu-id="88ed6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88ed6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ed6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ed6-130">-WhatIf</span></span>
<span data-ttu-id="88ed6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88ed6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88ed6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88ed6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ed6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ed6-133">-DefaultProfile</span></span>
<span data-ttu-id="88ed6-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88ed6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ed6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ed6-135">CommonParameters</span></span>
<span data-ttu-id="88ed6-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ed6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ed6-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ed6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ed6-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88ed6-138">INPUTS</span></span>

### <span data-ttu-id="88ed6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88ed6-139">System.String</span></span>
<span data-ttu-id="88ed6-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel; Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="88ed6-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="88ed6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88ed6-141">OUTPUTS</span></span>

### <span data-ttu-id="88ed6-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="88ed6-142">System.Object</span></span>

## <span data-ttu-id="88ed6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88ed6-143">NOTES</span></span>

## <span data-ttu-id="88ed6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88ed6-144">RELATED LINKS</span></span>

[<span data-ttu-id="88ed6-145">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="88ed6-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="88ed6-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="88ed6-148">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="88ed6-149">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="88ed6-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="88ed6-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="88ed6-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="88ed6-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
