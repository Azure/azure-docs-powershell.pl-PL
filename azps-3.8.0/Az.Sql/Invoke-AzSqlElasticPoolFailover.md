---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049719"
---
# <span data-ttu-id="744e6-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="744e6-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="744e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="744e6-102">SYNOPSIS</span></span>
<span data-ttu-id="744e6-103">Praca awaryjna z elastyczną pulą.</span><span class="sxs-lookup"><span data-stu-id="744e6-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="744e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="744e6-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="744e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="744e6-105">DESCRIPTION</span></span>
<span data-ttu-id="744e6-106">Polecenie cmdlet Invoke-AzSqlElasticPoolFailover tryb pracy awaryjnej puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="744e6-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="744e6-107">Po uruchomieniu tego polecenia cmdlet nastąpi przejście do trybu failover we wszystkich bazach danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="744e6-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="744e6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="744e6-108">EXAMPLES</span></span>

### <span data-ttu-id="744e6-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="744e6-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="744e6-110">To polecenie przejdzie w tryb pracy awaryjnej puli elastycznej o nazwie "ElasticPool01" na serwerze o nazwie "Server01".</span><span class="sxs-lookup"><span data-stu-id="744e6-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="744e6-111">Oznacza to, że przejęcie awaryjne będzie wykonywane we wszystkich bazach danych w puli elastycznej o nazwie "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="744e6-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="744e6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="744e6-112">PARAMETERS</span></span>

### <span data-ttu-id="744e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="744e6-113">-AsJob</span></span>
<span data-ttu-id="744e6-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="744e6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="744e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744e6-115">-DefaultProfile</span></span>
<span data-ttu-id="744e6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="744e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744e6-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="744e6-117">-ElasticPoolName</span></span>
<span data-ttu-id="744e6-118">Nazwa puli elastycznej SQL Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="744e6-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="744e6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="744e6-119">-Force</span></span>
<span data-ttu-id="744e6-120">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="744e6-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="744e6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="744e6-121">-PassThru</span></span>
<span data-ttu-id="744e6-122">Po udanym wykonaniu zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="744e6-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="744e6-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="744e6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="744e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="744e6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="744e6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="744e6-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="744e6-126">-ServerName</span></span>
<span data-ttu-id="744e6-127">Nazwa programu Azure SQL Server, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="744e6-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="744e6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="744e6-128">-Confirm</span></span>
<span data-ttu-id="744e6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="744e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744e6-130">-WhatIf</span></span>
<span data-ttu-id="744e6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="744e6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="744e6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="744e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="744e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744e6-133">CommonParameters</span></span>
<span data-ttu-id="744e6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744e6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="744e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744e6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="744e6-136">INPUTS</span></span>

### <span data-ttu-id="744e6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="744e6-137">System.String</span></span>

## <span data-ttu-id="744e6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="744e6-138">OUTPUTS</span></span>

## <span data-ttu-id="744e6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="744e6-139">NOTES</span></span>

## <span data-ttu-id="744e6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="744e6-140">RELATED LINKS</span></span>

[<span data-ttu-id="744e6-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="744e6-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="744e6-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="744e6-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="744e6-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="744e6-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="744e6-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="744e6-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="744e6-145">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="744e6-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="744e6-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="744e6-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="744e6-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="744e6-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="744e6-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="744e6-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)