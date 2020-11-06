---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550496"
---
# <span data-ttu-id="c9bff-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c9bff-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c9bff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9bff-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bff-103">Kończenie replikacji danych między bazą danych SQL a określoną pomocniczą bazą danych.</span><span class="sxs-lookup"><span data-stu-id="c9bff-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9bff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9bff-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9bff-105">DESCRIPTION</span></span>
<span data-ttu-id="c9bff-106">Polecenie cmdlet **Remove-AzureRmSqlDatabaseSecondary** wymusza zakończenie linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="c9bff-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="c9bff-107">To polecenie cmdlet zastępuje Stop-AzureSqlDatabaseCopy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bff-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="c9bff-108">Nie istnieje Synchronizacja replikacji przed zakończeniem.</span><span class="sxs-lookup"><span data-stu-id="c9bff-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="c9bff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9bff-109">EXAMPLES</span></span>

## <span data-ttu-id="c9bff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9bff-110">PARAMETERS</span></span>

### <span data-ttu-id="c9bff-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9bff-111">-DatabaseName</span></span>
<span data-ttu-id="c9bff-112">Określa nazwę podstawowej bazy danych SQL Azure z linkiem replikacji usuwanym przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bff-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bff-113">-DefaultProfile</span></span>
<span data-ttu-id="c9bff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9bff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9bff-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bff-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c9bff-116">Określa nazwę grupy zasobów partnera.</span><span class="sxs-lookup"><span data-stu-id="c9bff-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bff-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c9bff-117">-PartnerServerName</span></span>
<span data-ttu-id="c9bff-118">Określa nazwę serwera SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="c9bff-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bff-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9bff-120">Określa nazwę grupy zasobów, która jest skojarzona z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c9bff-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="c9bff-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c9bff-121">-ServerName</span></span>
<span data-ttu-id="c9bff-122">Określa nazwę serwera SQL z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c9bff-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="c9bff-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9bff-123">-Confirm</span></span>
<span data-ttu-id="c9bff-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9bff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bff-125">-WhatIf</span></span>
<span data-ttu-id="c9bff-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9bff-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9bff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9bff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bff-128">CommonParameters</span></span>
<span data-ttu-id="c9bff-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bff-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9bff-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bff-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9bff-131">INPUTS</span></span>

###  
<span data-ttu-id="c9bff-132">Do tego polecenia cmdlet można przepotokać wystąpienia obiektu **bazy danych** dla podstawowej lub pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c9bff-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="c9bff-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9bff-133">OUTPUTS</span></span>

###  
<span data-ttu-id="c9bff-134">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c9bff-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c9bff-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9bff-135">NOTES</span></span>

## <span data-ttu-id="c9bff-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9bff-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9bff-137">Nowe — AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c9bff-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="c9bff-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c9bff-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="c9bff-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c9bff-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
