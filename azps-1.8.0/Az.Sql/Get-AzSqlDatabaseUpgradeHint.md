---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707968"
---
# <span data-ttu-id="f48b2-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="f48b2-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="f48b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f48b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f48b2-103">Pobiera wskazówki dotyczące warstwy cenowej dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f48b2-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="f48b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f48b2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f48b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f48b2-106">Polecenie cmdlet **Get-AzSqlDatabaseUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej umożliwiające uaktualnienie bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f48b2-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="f48b2-107">Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i w firmie, uzyskują wskazówkę umożliwiającą uaktualnienie nowych warstw cenowych podstawowych, standardowych i Premium.</span><span class="sxs-lookup"><span data-stu-id="f48b2-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="f48b2-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f48b2-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f48b2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f48b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f48b2-110">Przykład 1: uzyskiwanie rekomendacji dla wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="f48b2-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f48b2-111">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="f48b2-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="f48b2-112">Przykład 2: uzyskiwanie rekomendacji dla konkretnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f48b2-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f48b2-113">To polecenie zwraca wskazówki dotyczące uaktualniania dla konkretnej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f48b2-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="f48b2-114">Przykład 3: uzyskiwanie rekomendacji dla wszystkich baz danych, które nie należą do puli Elastic Database</span><span class="sxs-lookup"><span data-stu-id="f48b2-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="f48b2-115">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych, które nie należą do puli Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="f48b2-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="f48b2-116">Przykład 4: uzyskiwanie rekomendacji dla wszystkich baz danych na serwerze przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="f48b2-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="f48b2-117">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01, których nazwy rozpoczynają się od "bazy danych".</span><span class="sxs-lookup"><span data-stu-id="f48b2-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="f48b2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f48b2-118">PARAMETERS</span></span>

### <span data-ttu-id="f48b2-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f48b2-119">-DatabaseName</span></span>
<span data-ttu-id="f48b2-120">Określa nazwę bazy danych SQL, dla której to polecenie cmdlet pobiera wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="f48b2-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="f48b2-121">Jeśli baza danych nie zostanie określona, to polecenie cmdlet będzie pobierać wskazówki dotyczące wszystkich baz danych na serwerze logicznym.</span><span class="sxs-lookup"><span data-stu-id="f48b2-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f48b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48b2-122">-DefaultProfile</span></span>
<span data-ttu-id="f48b2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f48b2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f48b2-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="f48b2-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="f48b2-125">Wskazuje, czy bazy danych w pulach Elastic Database są wykluczone z zwróconych rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="f48b2-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f48b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="f48b2-127">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="f48b2-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f48b2-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f48b2-128">-ServerName</span></span>
<span data-ttu-id="f48b2-129">Określa nazwę serwera obsługującego bazę danych, dla której ten aplet polecenia uzyskuje wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="f48b2-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="f48b2-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f48b2-130">-Confirm</span></span>
<span data-ttu-id="f48b2-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48b2-132">-WhatIf</span></span>
<span data-ttu-id="f48b2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f48b2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f48b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48b2-135">CommonParameters</span></span>
<span data-ttu-id="f48b2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48b2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f48b2-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48b2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f48b2-138">INPUTS</span></span>

### <span data-ttu-id="f48b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f48b2-139">System.String</span></span>

### <span data-ttu-id="f48b2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f48b2-140">System.Boolean</span></span>

## <span data-ttu-id="f48b2-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f48b2-141">OUTPUTS</span></span>

### <span data-ttu-id="f48b2-142">Microsoft. Azure. Management. SQL. LegacySdk. MODELES. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="f48b2-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="f48b2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f48b2-143">NOTES</span></span>

## <span data-ttu-id="f48b2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f48b2-144">RELATED LINKS</span></span>

[<span data-ttu-id="f48b2-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f48b2-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="f48b2-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="f48b2-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

