---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887697"
---
# <span data-ttu-id="757d7-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="757d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="757d7-102">SYNOPSIS</span></span>
<span data-ttu-id="757d7-103">Wykonuje przejście do trybu failover grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="757d7-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="757d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="757d7-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="757d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="757d7-105">DESCRIPTION</span></span>
<span data-ttu-id="757d7-106">To polecenie umożliwia zamianę ról serwerów w grupie pracy awaryjnej i przełączanie wszystkich pomocniczych baz danych na rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="757d7-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="757d7-107">Wszystkie nowe sesje TDS są automatycznie przekierowywane do serwera pomocniczego po odświeżeniu pamięci podręcznej klienta DNS.</span><span class="sxs-lookup"><span data-stu-id="757d7-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="757d7-108">Po powrocie do oryginalnego serwera podstawowego wszystkie uprzednio podstawowe bazy danych zostaną przełączone do roli pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="757d7-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="757d7-109">Aby wykonać to polecenie, należy użyć serwera pomocniczego grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="757d7-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="757d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="757d7-110">EXAMPLES</span></span>

### <span data-ttu-id="757d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="757d7-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="757d7-112">Wygeneruj operację przełączania awaryjnego umożliwiającą utratę danych przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="757d7-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="757d7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="757d7-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="757d7-114">Wydaj optymalną operację przejęcia awaryjnego, która zakończy się powodzeniem bez utraty danych lub niepowodzenia i wycofania.</span><span class="sxs-lookup"><span data-stu-id="757d7-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="757d7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="757d7-115">PARAMETERS</span></span>

### <span data-ttu-id="757d7-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="757d7-116">-AllowDataLoss</span></span>
<span data-ttu-id="757d7-117">Ukończ pracę awaryjną, nawet jeśli to może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="757d7-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="757d7-118">Umożliwi to kontynuowanie pracy awaryjnej nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="757d7-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="757d7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="757d7-119">-AsJob</span></span>
<span data-ttu-id="757d7-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="757d7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="757d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757d7-121">-DefaultProfile</span></span>
<span data-ttu-id="757d7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="757d7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="757d7-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="757d7-123">-FailoverGroupName</span></span>
<span data-ttu-id="757d7-124">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="757d7-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="757d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="757d7-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="757d7-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="757d7-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="757d7-127">-ServerName</span></span>
<span data-ttu-id="757d7-128">Nazwa pomocniczego serwera bazy danych SQL platformy Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="757d7-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="757d7-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="757d7-129">-Confirm</span></span>
<span data-ttu-id="757d7-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757d7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757d7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757d7-131">-WhatIf</span></span>
<span data-ttu-id="757d7-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757d7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757d7-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="757d7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757d7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757d7-134">CommonParameters</span></span>
<span data-ttu-id="757d7-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757d7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757d7-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="757d7-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757d7-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="757d7-137">INPUTS</span></span>

### <span data-ttu-id="757d7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="757d7-138">System.String</span></span>

## <span data-ttu-id="757d7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="757d7-139">OUTPUTS</span></span>

### <span data-ttu-id="757d7-140">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="757d7-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="757d7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="757d7-141">NOTES</span></span>

## <span data-ttu-id="757d7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="757d7-142">RELATED LINKS</span></span>

[<span data-ttu-id="757d7-143">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="757d7-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="757d7-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="757d7-146">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="757d7-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="757d7-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="757d7-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="757d7-149">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="757d7-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
