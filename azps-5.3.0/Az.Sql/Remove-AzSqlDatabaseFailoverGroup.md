---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498289"
---
# <span data-ttu-id="c194c-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c194c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c194c-102">SYNOPSIS</span></span>
<span data-ttu-id="c194c-103">Usuwa grupę trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c194c-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="c194c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c194c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c194c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c194c-105">DESCRIPTION</span></span>
<span data-ttu-id="c194c-106">To polecenie usuwa grupę pracy awaryjnej o określonej nazwie, pozostawiając wszystkie bazy danych i relacje replikacji bez zmian.</span><span class="sxs-lookup"><span data-stu-id="c194c-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="c194c-107">Punkt końcowy odbiornika zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="c194c-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="c194c-108">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="c194c-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="c194c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c194c-109">EXAMPLES</span></span>

### <span data-ttu-id="c194c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c194c-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="c194c-111">Usuwanie grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="c194c-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="c194c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c194c-112">PARAMETERS</span></span>

### <span data-ttu-id="c194c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c194c-113">-DefaultProfile</span></span>
<span data-ttu-id="c194c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c194c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c194c-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c194c-115">-FailoverGroupName</span></span>
<span data-ttu-id="c194c-116">Nazwa grupy trybu failover bazy danych SQL Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c194c-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="c194c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c194c-117">-Force</span></span>
<span data-ttu-id="c194c-118">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="c194c-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="c194c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c194c-119">-ResourceGroupName</span></span>
<span data-ttu-id="c194c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c194c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c194c-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c194c-121">-ServerName</span></span>
<span data-ttu-id="c194c-122">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c194c-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c194c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c194c-123">-Confirm</span></span>
<span data-ttu-id="c194c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c194c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c194c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c194c-125">-WhatIf</span></span>
<span data-ttu-id="c194c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c194c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c194c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c194c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c194c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c194c-128">CommonParameters</span></span>
<span data-ttu-id="c194c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c194c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c194c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c194c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c194c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c194c-131">INPUTS</span></span>

### <span data-ttu-id="c194c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c194c-132">System.String</span></span>

## <span data-ttu-id="c194c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c194c-133">OUTPUTS</span></span>

### <span data-ttu-id="c194c-134">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c194c-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c194c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c194c-135">NOTES</span></span>

## <span data-ttu-id="c194c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c194c-136">RELATED LINKS</span></span>

[<span data-ttu-id="c194c-137">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c194c-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c194c-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c194c-140">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c194c-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c194c-142">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c194c-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c194c-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c194c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
