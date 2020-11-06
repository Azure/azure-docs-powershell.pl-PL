---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: a8f147b4e2c8a1f4525585f8622b7195ed759022
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548492"
---
# <span data-ttu-id="4381b-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="4381b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4381b-102">SYNOPSIS</span></span>
<span data-ttu-id="4381b-103">Usuwa co najmniej jeden z baz danych z grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4381b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4381b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4381b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4381b-105">DESCRIPTION</span></span>
<span data-ttu-id="4381b-106">Usuwa co najmniej jeden z baz danych z określonej grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="4381b-107">Bazy danych i relacje replikacji pozostają nienaruszone, ale nie będą już dostępne w punktach końcowych grup pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="4381b-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="4381b-108">Aby uzyskać obiekty bazy danych, do których ma zostać wypełniony parametr "-Database", użyj (na przykład) polecenia cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="4381b-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="4381b-109">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="4381b-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="4381b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4381b-110">EXAMPLES</span></span>

### <span data-ttu-id="4381b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4381b-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4381b-112">To polecenie umożliwia usunięcie jednej bazy danych z grupy trybu failover przez przejście do niej.</span><span class="sxs-lookup"><span data-stu-id="4381b-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="4381b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4381b-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="4381b-114">To polecenie usuwa wszystkie bazy danych z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="4381b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4381b-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="4381b-116">To polecenie usuwa wszystkie bazy danych z grupy elastycznej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="4381b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4381b-117">PARAMETERS</span></span>

### <span data-ttu-id="4381b-118">-Database</span><span class="sxs-lookup"><span data-stu-id="4381b-118">-Database</span></span>
<span data-ttu-id="4381b-119">Co najmniej jedna baza danych SQL Azure na serwerze podstawowym grupy trybu failover do usunięcia z grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="4381b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4381b-120">-DefaultProfile</span></span>
<span data-ttu-id="4381b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4381b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4381b-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4381b-122">-FailoverGroupName</span></span>
<span data-ttu-id="4381b-123">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4381b-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4381b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4381b-124">-Force</span></span>
<span data-ttu-id="4381b-125">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="4381b-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4381b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4381b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4381b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4381b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4381b-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4381b-128">-ServerName</span></span>
<span data-ttu-id="4381b-129">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="4381b-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4381b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4381b-130">-Confirm</span></span>
<span data-ttu-id="4381b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4381b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4381b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4381b-132">-WhatIf</span></span>
<span data-ttu-id="4381b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4381b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4381b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4381b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4381b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4381b-135">CommonParameters</span></span>
<span data-ttu-id="4381b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4381b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4381b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4381b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4381b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4381b-138">INPUTS</span></span>

### <span data-ttu-id="4381b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4381b-139">System.String</span></span>

### <span data-ttu-id="4381b-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel; Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4381b-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4381b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4381b-141">OUTPUTS</span></span>

### <span data-ttu-id="4381b-142">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4381b-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4381b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4381b-143">NOTES</span></span>

## <span data-ttu-id="4381b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4381b-144">RELATED LINKS</span></span>

[<span data-ttu-id="4381b-145">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4381b-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4381b-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4381b-148">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4381b-149">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4381b-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4381b-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4381b-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4381b-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
