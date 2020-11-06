---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 45be8d0ef10b040fd27a714444bb60bbf6a69951
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552304"
---
# <span data-ttu-id="e1ae5-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="e1ae5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ae5-103">Wykonuje przejście do trybu failover grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ae5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1ae5-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ae5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ae5-106">To polecenie umożliwia zamianę ról serwerów w grupie pracy awaryjnej i przełączanie wszystkich pomocniczych baz danych na rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="e1ae5-107">Wszystkie nowe sesje TDS są automatycznie przekierowywane do serwera pomocniczego po odświeżeniu pamięci podręcznej klienta DNS.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="e1ae5-108">Po powrocie do oryginalnego serwera podstawowego wszystkie uprzednio podstawowe bazy danych zostaną przełączone do roli pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="e1ae5-109">Aby wykonać to polecenie, należy użyć serwera pomocniczego grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="e1ae5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1ae5-110">EXAMPLES</span></span>

### <span data-ttu-id="e1ae5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1ae5-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="e1ae5-112">Wygeneruj operację przełączania awaryjnego umożliwiającą utratę danych przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="e1ae5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1ae5-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="e1ae5-114">Wydaj optymalną operację przejęcia awaryjnego, która zakończy się powodzeniem bez utraty danych lub niepowodzenia i wycofania.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="e1ae5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1ae5-115">PARAMETERS</span></span>

### <span data-ttu-id="e1ae5-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="e1ae5-116">-AllowDataLoss</span></span>
<span data-ttu-id="e1ae5-117">Ukończ pracę awaryjną, nawet jeśli to może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="e1ae5-118">Umożliwi to kontynuowanie pracy awaryjnej nawet wtedy, gdy podstawowa baza danych jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="e1ae5-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ae5-119">-FailoverGroupName</span></span>
<span data-ttu-id="e1ae5-120">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="e1ae5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ae5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1ae5-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e1ae5-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e1ae5-123">-ServerName</span></span>
<span data-ttu-id="e1ae5-124">Nazwa pomocniczego serwera bazy danych SQL platformy Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-124">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="e1ae5-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1ae5-125">-Confirm</span></span>
<span data-ttu-id="e1ae5-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ae5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ae5-127">-WhatIf</span></span>
<span data-ttu-id="e1ae5-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ae5-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ae5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ae5-130">-DefaultProfile</span></span>
<span data-ttu-id="e1ae5-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ae5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ae5-132">CommonParameters</span></span>
<span data-ttu-id="e1ae5-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ae5-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ae5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ae5-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ae5-135">INPUTS</span></span>

### <span data-ttu-id="e1ae5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ae5-136">System.String</span></span>

## <span data-ttu-id="e1ae5-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1ae5-137">OUTPUTS</span></span>

### <span data-ttu-id="e1ae5-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="e1ae5-138">System.Object</span></span>

## <span data-ttu-id="e1ae5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1ae5-139">NOTES</span></span>

## <span data-ttu-id="e1ae5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1ae5-140">RELATED LINKS</span></span>

[<span data-ttu-id="e1ae5-141">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-141">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e1ae5-142">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-142">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e1ae5-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e1ae5-144">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="e1ae5-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="e1ae5-146">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e1ae5-146">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e1ae5-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e1ae5-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
