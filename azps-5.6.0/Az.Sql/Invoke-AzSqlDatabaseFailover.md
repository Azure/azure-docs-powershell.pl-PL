---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 23df8f00c91cfabf4ad01b5dd641069f159eb064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987540"
---
# <span data-ttu-id="1c970-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="1c970-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="1c970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c970-102">SYNOPSIS</span></span>
<span data-ttu-id="1c970-103">Trybu failovers bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1c970-103">Failovers a database.</span></span>

## <span data-ttu-id="1c970-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c970-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c970-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c970-105">DESCRIPTION</span></span>
<span data-ttu-id="1c970-106">Polecenie Invoke-AzSqlDatabaseFailover trybu failovers bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1c970-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="1c970-107">Jeśli baza danych znajduje się w elastycznej puli, to polecenie spowoduje trybu failover danej bazy danych bez wpływu na pozostałe bazy danych w tej samej puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="1c970-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="1c970-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c970-108">EXAMPLES</span></span>

### <span data-ttu-id="1c970-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c970-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1c970-110">To polecenie spowoduje trybu failover podstawowej repliki bazy danych o nazwie "Database01" na serwerze o nazwie "Server01"</span><span class="sxs-lookup"><span data-stu-id="1c970-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="1c970-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1c970-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="1c970-112">To polecenie spowoduje trybu failover czytelnej repliki pomocniczej bazy danych o nazwie "Database01" na serwerze o nazwie "Server01"</span><span class="sxs-lookup"><span data-stu-id="1c970-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="1c970-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c970-113">PARAMETERS</span></span>

### <span data-ttu-id="1c970-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1c970-114">-AsJob</span></span>
<span data-ttu-id="1c970-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1c970-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c970-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c970-116">-DatabaseName</span></span>
<span data-ttu-id="1c970-117">Nazwa usługi Azure SQL Database do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="1c970-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="1c970-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c970-118">-DefaultProfile</span></span>
<span data-ttu-id="1c970-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c970-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c970-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1c970-120">-Force</span></span>
<span data-ttu-id="1c970-121">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="1c970-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1c970-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c970-122">-PassThru</span></span>
<span data-ttu-id="1c970-123">Po pomyślnym wykonaniu zwraca wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="1c970-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="1c970-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1c970-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c970-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="1c970-125">-ReadableSecondary</span></span>
<span data-ttu-id="1c970-126">Failover the readable secondary replica instead of the default primary replica</span><span class="sxs-lookup"><span data-stu-id="1c970-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="1c970-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c970-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c970-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c970-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c970-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c970-129">-ServerName</span></span>
<span data-ttu-id="1c970-130">Nazwa serwera Azure SQL Database Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="1c970-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="1c970-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c970-131">-Confirm</span></span>
<span data-ttu-id="1c970-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1c970-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c970-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c970-133">-WhatIf</span></span>
<span data-ttu-id="1c970-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c970-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c970-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1c970-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c970-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c970-136">CommonParameters</span></span>
<span data-ttu-id="1c970-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c970-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c970-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c970-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c970-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c970-139">INPUTS</span></span>

### <span data-ttu-id="1c970-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1c970-140">System.String</span></span>

## <span data-ttu-id="1c970-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c970-141">OUTPUTS</span></span>

## <span data-ttu-id="1c970-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c970-142">NOTES</span></span>

## <span data-ttu-id="1c970-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c970-143">RELATED LINKS</span></span>

[<span data-ttu-id="1c970-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1c970-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="1c970-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="1c970-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="1c970-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1c970-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1c970-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1c970-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c970-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1c970-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1c970-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
