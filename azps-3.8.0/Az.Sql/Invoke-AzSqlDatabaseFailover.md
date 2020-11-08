---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049724"
---
# <span data-ttu-id="30759-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="30759-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="30759-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30759-102">SYNOPSIS</span></span>
<span data-ttu-id="30759-103">Praca awaryjna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="30759-103">Failovers a database.</span></span>

## <span data-ttu-id="30759-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30759-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30759-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30759-105">DESCRIPTION</span></span>
<span data-ttu-id="30759-106">Polecenie cmdlet Invoke-AzSqlDatabaseFailover tryb failover bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="30759-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="30759-107">Jeśli baza danych znajduje się w puli elastycznej, to polecenie przejdzie w tryb failover dla danej bazy danych bez wpływu na inne bazy danych w tej samej puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="30759-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="30759-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30759-108">EXAMPLES</span></span>

### <span data-ttu-id="30759-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30759-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="30759-110">To polecenie przejdzie w tryb failover replika podstawowa bazy danych o nazwie "Database01" na serwerze o nazwie "Server01".</span><span class="sxs-lookup"><span data-stu-id="30759-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="30759-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="30759-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="30759-112">To polecenie przejdzie w tryb failover do czytelnej repliki pomocniczej bazy danych o nazwie "Database01" na serwerze o nazwie "Server01".</span><span class="sxs-lookup"><span data-stu-id="30759-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="30759-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30759-113">PARAMETERS</span></span>

### <span data-ttu-id="30759-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30759-114">-AsJob</span></span>
<span data-ttu-id="30759-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="30759-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30759-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30759-116">-DatabaseName</span></span>
<span data-ttu-id="30759-117">Nazwa bazy danych SQL Azure do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="30759-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="30759-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30759-118">-DefaultProfile</span></span>
<span data-ttu-id="30759-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30759-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30759-120">-Force</span><span class="sxs-lookup"><span data-stu-id="30759-120">-Force</span></span>
<span data-ttu-id="30759-121">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="30759-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="30759-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30759-122">-PassThru</span></span>
<span data-ttu-id="30759-123">Po udanym wykonaniu zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="30759-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="30759-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="30759-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30759-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="30759-125">-ReadableSecondary</span></span>
<span data-ttu-id="30759-126">Przejmowanie awaryjnej repliki pomocniczej zamiast domyślnej repliki podstawowej</span><span class="sxs-lookup"><span data-stu-id="30759-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="30759-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30759-127">-ResourceGroupName</span></span>
<span data-ttu-id="30759-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="30759-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="30759-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="30759-129">-ServerName</span></span>
<span data-ttu-id="30759-130">Nazwa serwera bazy danych SQL Azure, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="30759-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="30759-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30759-131">-Confirm</span></span>
<span data-ttu-id="30759-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30759-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30759-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30759-133">-WhatIf</span></span>
<span data-ttu-id="30759-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30759-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30759-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30759-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30759-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30759-136">CommonParameters</span></span>
<span data-ttu-id="30759-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30759-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30759-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30759-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30759-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30759-139">INPUTS</span></span>

### <span data-ttu-id="30759-140">System. String</span><span class="sxs-lookup"><span data-stu-id="30759-140">System.String</span></span>

## <span data-ttu-id="30759-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30759-141">OUTPUTS</span></span>

## <span data-ttu-id="30759-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30759-142">NOTES</span></span>

## <span data-ttu-id="30759-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30759-143">RELATED LINKS</span></span>

[<span data-ttu-id="30759-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="30759-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="30759-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="30759-146">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="30759-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="30759-148">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="30759-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="30759-150">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30759-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="30759-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="30759-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
