---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a6fd65ed16797d3d497160f7f7d9d52f17bd2f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550512"
---
# <span data-ttu-id="83b9b-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="83b9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="83b9b-103">Usuwa grupę trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="83b9b-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83b9b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83b9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="83b9b-106">To polecenie usuwa grupę pracy awaryjnej o określonej nazwie, pozostawiając wszystkie bazy danych i relacje replikacji bez zmian.</span><span class="sxs-lookup"><span data-stu-id="83b9b-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="83b9b-107">Punkt końcowy odbiornika zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="83b9b-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="83b9b-108">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="83b9b-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="83b9b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83b9b-109">EXAMPLES</span></span>

### <span data-ttu-id="83b9b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83b9b-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="83b9b-111">Usuwanie grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="83b9b-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="83b9b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83b9b-112">PARAMETERS</span></span>

### <span data-ttu-id="83b9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b9b-113">-DefaultProfile</span></span>
<span data-ttu-id="83b9b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="83b9b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="83b9b-115">-FailoverGroupName</span></span>
<span data-ttu-id="83b9b-116">Nazwa grupy trybu failover bazy danych SQL Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="83b9b-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="83b9b-117">-Force</span></span>
<span data-ttu-id="83b9b-118">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="83b9b-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b9b-119">-ResourceGroupName</span></span>
<span data-ttu-id="83b9b-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83b9b-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="83b9b-121">-ServerName</span></span>
<span data-ttu-id="83b9b-122">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="83b9b-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83b9b-123">-Confirm</span></span>
<span data-ttu-id="83b9b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b9b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b9b-125">-WhatIf</span></span>
<span data-ttu-id="83b9b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b9b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b9b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83b9b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b9b-128">CommonParameters</span></span>
<span data-ttu-id="83b9b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b9b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b9b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b9b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83b9b-131">INPUTS</span></span>

### <span data-ttu-id="83b9b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="83b9b-132">System.String</span></span>

## <span data-ttu-id="83b9b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83b9b-133">OUTPUTS</span></span>

### <span data-ttu-id="83b9b-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="83b9b-134">System.Object</span></span>

## <span data-ttu-id="83b9b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83b9b-135">NOTES</span></span>

## <span data-ttu-id="83b9b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83b9b-136">RELATED LINKS</span></span>

[<span data-ttu-id="83b9b-137">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="83b9b-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="83b9b-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="83b9b-140">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="83b9b-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="83b9b-142">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9b-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="83b9b-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="83b9b-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
