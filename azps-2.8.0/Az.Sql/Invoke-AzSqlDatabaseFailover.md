---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887418"
---
# <span data-ttu-id="a8b40-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="a8b40-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="a8b40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8b40-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b40-103">Praca awaryjna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a8b40-103">Failovers a database.</span></span>

## <span data-ttu-id="a8b40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8b40-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8b40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8b40-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b40-106">Polecenie cmdlet Invoke-AzSqlDatabaseFailover tryb failover bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a8b40-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="a8b40-107">Jeśli baza danych znajduje się w puli elastycznej, to polecenie przejdzie w tryb failover dla danej bazy danych bez wpływu na inne bazy danych w tej samej puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="a8b40-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="a8b40-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8b40-108">EXAMPLES</span></span>

### <span data-ttu-id="a8b40-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8b40-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a8b40-110">To polecenie przeprowadzi awaryjnie bazę danych o nazwie "Database01" na serwerze o nazwie "Server01".</span><span class="sxs-lookup"><span data-stu-id="a8b40-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="a8b40-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8b40-111">PARAMETERS</span></span>

### <span data-ttu-id="a8b40-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8b40-112">-AsJob</span></span>
<span data-ttu-id="a8b40-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a8b40-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8b40-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8b40-114">-DatabaseName</span></span>
<span data-ttu-id="a8b40-115">Nazwa bazy danych SQL Azure do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="a8b40-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="a8b40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b40-116">-DefaultProfile</span></span>
<span data-ttu-id="a8b40-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b40-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a8b40-118">-Force</span></span>
<span data-ttu-id="a8b40-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="a8b40-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a8b40-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8b40-120">-PassThru</span></span>
<span data-ttu-id="a8b40-121">Po udanym wykonaniu zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="a8b40-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="a8b40-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a8b40-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8b40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b40-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8b40-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8b40-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8b40-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a8b40-125">-ServerName</span></span>
<span data-ttu-id="a8b40-126">Nazwa serwera bazy danych SQL Azure, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="a8b40-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="a8b40-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8b40-127">-Confirm</span></span>
<span data-ttu-id="a8b40-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b40-129">-WhatIf</span></span>
<span data-ttu-id="a8b40-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b40-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8b40-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8b40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b40-132">CommonParameters</span></span>
<span data-ttu-id="a8b40-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b40-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8b40-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b40-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8b40-135">INPUTS</span></span>

### <span data-ttu-id="a8b40-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a8b40-136">System.String</span></span>

## <span data-ttu-id="a8b40-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8b40-137">OUTPUTS</span></span>

## <span data-ttu-id="a8b40-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8b40-138">NOTES</span></span>

## <span data-ttu-id="a8b40-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8b40-139">RELATED LINKS</span></span>

[<span data-ttu-id="a8b40-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="a8b40-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="a8b40-142">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-144">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-146">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8b40-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="a8b40-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a8b40-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
