---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 08192eb96b7c0a2dde84a51cf49f3b96e5429ffc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2020
ms.locfileid: "94224094"
---
# <span data-ttu-id="6d7cb-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="6d7cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7cb-103">Wykonuje przejście do trybu failover grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6d7cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d7cb-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d7cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="6d7cb-106">To polecenie umożliwia zamianę ról serwerów w grupie pracy awaryjnej i przełączanie wszystkich pomocniczych baz danych na rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="6d7cb-107">Wszystkie nowe sesje TDS są automatycznie przekierowywane do serwera pomocniczego po odświeżeniu pamięci podręcznej klienta DNS.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="6d7cb-108">Po powrocie do oryginalnego serwera podstawowego wszystkie uprzednio podstawowe bazy danych zostaną przełączone do roli pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="6d7cb-109">Aby wykonać to polecenie, należy użyć serwera pomocniczego grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="6d7cb-110">Jeśli nie określono parametru AllowDataLoss, to polecenie czeka na przełączenie obu ról.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="6d7cb-111">Jeśli parametr AllowDataLoss jest określony, polecenie będzie oczekiwać tylko do momentu, aż nowy podstawowy przyjmie swoją rolę.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="6d7cb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d7cb-112">EXAMPLES</span></span>

### <span data-ttu-id="6d7cb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d7cb-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="6d7cb-114">Wygeneruj operację przełączania awaryjnego umożliwiającą utratę danych przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="6d7cb-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6d7cb-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="6d7cb-116">Wydaj optymalną operację przejęcia awaryjnego, która zakończy się powodzeniem bez utraty danych lub niepowodzenia i wycofania.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="6d7cb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d7cb-117">PARAMETERS</span></span>

### <span data-ttu-id="6d7cb-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6d7cb-118">-AllowDataLoss</span></span>
<span data-ttu-id="6d7cb-119">Ukończ pracę awaryjną, nawet jeśli to może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="6d7cb-120">Umożliwi to kontynuowanie pracy awaryjnej nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7cb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d7cb-121">-AsJob</span></span>
<span data-ttu-id="6d7cb-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d7cb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d7cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7cb-123">-DefaultProfile</span></span>
<span data-ttu-id="6d7cb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d7cb-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d7cb-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7cb-125">-FailoverGroupName</span></span>
<span data-ttu-id="6d7cb-126">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d7cb-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d7cb-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6d7cb-129">-ServerName</span></span>
<span data-ttu-id="6d7cb-130">Nazwa pomocniczego serwera bazy danych SQL platformy Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="6d7cb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d7cb-131">-Confirm</span></span>
<span data-ttu-id="6d7cb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d7cb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7cb-133">-WhatIf</span></span>
<span data-ttu-id="6d7cb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7cb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d7cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7cb-136">CommonParameters</span></span>
<span data-ttu-id="6d7cb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7cb-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d7cb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7cb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d7cb-139">INPUTS</span></span>

### <span data-ttu-id="6d7cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7cb-140">System.String</span></span>

## <span data-ttu-id="6d7cb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d7cb-141">OUTPUTS</span></span>

### <span data-ttu-id="6d7cb-142">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6d7cb-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6d7cb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d7cb-143">NOTES</span></span>

## <span data-ttu-id="6d7cb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d7cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d7cb-145">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6d7cb-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6d7cb-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6d7cb-148">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="6d7cb-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6d7cb-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6d7cb-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6d7cb-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6d7cb-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
