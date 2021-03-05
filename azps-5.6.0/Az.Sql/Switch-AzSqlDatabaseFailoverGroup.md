---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a8ad9a3925ccf1c0f56ce9be6a962d667f122307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992307"
---
# <span data-ttu-id="3c176-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="3c176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c176-102">SYNOPSIS</span></span>
<span data-ttu-id="3c176-103">Wykonuje failover grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3c176-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="3c176-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c176-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c176-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c176-105">DESCRIPTION</span></span>
<span data-ttu-id="3c176-106">To polecenie zamienia role serwerów w grupie trybu failover i przełącza wszystkie pomocnicze bazy danych do roli podstawowej.</span><span class="sxs-lookup"><span data-stu-id="3c176-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="3c176-107">Wszystkie nowe sesje TDS są automatycznie kierowane ponownie do serwera pomocniczego po odświeżeniu pamięci podręcznej klienta DNS.</span><span class="sxs-lookup"><span data-stu-id="3c176-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="3c176-108">Gdy oryginalny serwer podstawowy powróci do trybu online, wszystkie wcześniej podstawowe bazy danych na tym serwerze zostaną przełączoną do roli pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="3c176-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="3c176-109">Aby wykonać to polecenie, należy użyć serwera pomocniczego grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3c176-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="3c176-110">Jeśli parametr AllowDataLoss nie jest określony, to polecenie czeka, aż obie role zostaną przełączone.</span><span class="sxs-lookup"><span data-stu-id="3c176-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="3c176-111">Jeśli parametr AllowDataLoss jest określony, polecenie będzie oczekiwać tylko do momentu, aż nowa podstawowa przyjmie swoją rolę.</span><span class="sxs-lookup"><span data-stu-id="3c176-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="3c176-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c176-112">EXAMPLES</span></span>

### <span data-ttu-id="3c176-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c176-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="3c176-114">Problem z operacją trybu failover pozwalającą na utratę danych za pomocą rur w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3c176-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="3c176-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3c176-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="3c176-116">Omiń operację trybu failover o najlepszym namysłzie, która zakończy się powodzeniem bez utraty danych lub nie zakończy się niepowodzeniem i zostanie wycofana.</span><span class="sxs-lookup"><span data-stu-id="3c176-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="3c176-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c176-117">PARAMETERS</span></span>

### <span data-ttu-id="3c176-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="3c176-118">-AllowDataLoss</span></span>
<span data-ttu-id="3c176-119">Ukończ trybu failover, nawet jeśli spowoduje to utratę danych.</span><span class="sxs-lookup"><span data-stu-id="3c176-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="3c176-120">Umożliwi to kontynuowanie trybu failover nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="3c176-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="3c176-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3c176-121">-AsJob</span></span>
<span data-ttu-id="3c176-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3c176-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c176-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c176-123">-DefaultProfile</span></span>
<span data-ttu-id="3c176-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3c176-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c176-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3c176-125">-FailoverGroupName</span></span>
<span data-ttu-id="3c176-126">Nazwa grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3c176-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="3c176-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c176-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c176-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c176-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c176-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c176-129">-ServerName</span></span>
<span data-ttu-id="3c176-130">Nazwa pomocniczego serwera usługi Azure SQL Database Server grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3c176-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3c176-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c176-131">-Confirm</span></span>
<span data-ttu-id="3c176-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c176-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c176-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c176-133">-WhatIf</span></span>
<span data-ttu-id="3c176-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c176-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c176-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c176-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c176-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c176-136">CommonParameters</span></span>
<span data-ttu-id="3c176-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c176-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c176-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c176-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c176-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c176-139">INPUTS</span></span>

### <span data-ttu-id="3c176-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3c176-140">System.String</span></span>

## <span data-ttu-id="3c176-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c176-141">OUTPUTS</span></span>

### <span data-ttu-id="3c176-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="3c176-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="3c176-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c176-143">NOTES</span></span>

## <span data-ttu-id="3c176-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c176-144">RELATED LINKS</span></span>

[<span data-ttu-id="3c176-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3c176-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3c176-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3c176-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="3c176-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="3c176-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c176-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3c176-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3c176-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
