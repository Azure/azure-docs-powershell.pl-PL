---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201466"
---
# <span data-ttu-id="8692c-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="8692c-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="8692c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8692c-102">SYNOPSIS</span></span>
<span data-ttu-id="8692c-103">Trybu failovers bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8692c-103">Failovers a database.</span></span>

## <span data-ttu-id="8692c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8692c-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8692c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8692c-105">DESCRIPTION</span></span>
<span data-ttu-id="8692c-106">Polecenie Invoke-AzSqlDatabaseFailover trybu failovers bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8692c-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="8692c-107">Jeśli baza danych znajduje się w elastycznej puli, to polecenie spowoduje trybu failover danej bazy danych bez wpływu na pozostałe bazy danych w tej samej puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="8692c-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="8692c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8692c-108">EXAMPLES</span></span>

### <span data-ttu-id="8692c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8692c-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8692c-110">To polecenie spowoduje trybu failover podstawowej repliki bazy danych o nazwie "Database01" na serwerze o nazwie "Serwer01".</span><span class="sxs-lookup"><span data-stu-id="8692c-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="8692c-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8692c-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="8692c-112">To polecenie spowoduje trybu failover czytelnej repliki pomocniczej bazy danych o nazwie "Database01" na serwerze o nazwie "Server01"</span><span class="sxs-lookup"><span data-stu-id="8692c-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="8692c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8692c-113">PARAMETERS</span></span>

### <span data-ttu-id="8692c-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8692c-114">-AsJob</span></span>
<span data-ttu-id="8692c-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8692c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8692c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8692c-116">-DatabaseName</span></span>
<span data-ttu-id="8692c-117">Nazwa usługi Azure SQL Database do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8692c-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="8692c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8692c-118">-DefaultProfile</span></span>
<span data-ttu-id="8692c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8692c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8692c-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8692c-120">-Force</span></span>
<span data-ttu-id="8692c-121">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="8692c-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8692c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8692c-122">-PassThru</span></span>
<span data-ttu-id="8692c-123">Po pomyślnym wykonaniu zwraca wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="8692c-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="8692c-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8692c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8692c-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="8692c-125">-ReadableSecondary</span></span>
<span data-ttu-id="8692c-126">Failover the readable secondary replica instead of the default primary replica</span><span class="sxs-lookup"><span data-stu-id="8692c-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="8692c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8692c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8692c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8692c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8692c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8692c-129">-ServerName</span></span>
<span data-ttu-id="8692c-130">Nazwa serwera Azure SQL Database Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="8692c-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="8692c-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8692c-131">-Confirm</span></span>
<span data-ttu-id="8692c-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8692c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8692c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8692c-133">-WhatIf</span></span>
<span data-ttu-id="8692c-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8692c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8692c-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8692c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8692c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8692c-136">CommonParameters</span></span>
<span data-ttu-id="8692c-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8692c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8692c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8692c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8692c-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8692c-139">INPUTS</span></span>

### <span data-ttu-id="8692c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8692c-140">System.String</span></span>

## <span data-ttu-id="8692c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8692c-141">OUTPUTS</span></span>

## <span data-ttu-id="8692c-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8692c-142">NOTES</span></span>

## <span data-ttu-id="8692c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8692c-143">RELATED LINKS</span></span>

[<span data-ttu-id="8692c-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8692c-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="8692c-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="8692c-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8692c-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8692c-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8692c-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8692c-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8692c-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8692c-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8692c-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
