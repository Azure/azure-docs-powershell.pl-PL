---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014673"
---
# <span data-ttu-id="4a74a-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="4a74a-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="4a74a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a74a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a74a-103">Pobiera wskazówki dotyczące warstwy cenowej dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4a74a-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="4a74a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a74a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a74a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a74a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a74a-106">Polecenie **cmdlet Get-AzSqlDatabaseUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej dotyczące uaktualniania usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4a74a-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="4a74a-107">Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i dla firm, zawierają wskazówkę, aby uaktualnić do nowej warstwy cenowej Basic, Standard lub Premium.</span><span class="sxs-lookup"><span data-stu-id="4a74a-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="4a74a-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4a74a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4a74a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a74a-109">EXAMPLES</span></span>

### <span data-ttu-id="4a74a-110">Przykład 1. Uzyskiwanie rekomendacji dotyczących wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="4a74a-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="4a74a-111">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4a74a-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="4a74a-112">Przykład 2. Uzyskiwanie rekomendacji dotyczących konkretnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4a74a-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4a74a-113">To polecenie zwraca wskazówki dotyczące uaktualniania dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4a74a-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="4a74a-114">Przykład 3. Uzyskiwanie zalecenia dla wszystkich baz danych, które nie znajdują się w elastycznej puli baz danych</span><span class="sxs-lookup"><span data-stu-id="4a74a-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="4a74a-115">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych, które nie znajdują się w elastycznej puli baz danych.</span><span class="sxs-lookup"><span data-stu-id="4a74a-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="4a74a-116">Przykład 4. Uzyskiwanie rekomendacji dotyczących wszystkich baz danych na serwerze przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="4a74a-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="4a74a-117">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01, których nazwy zaczynają się od "Bazy danych".</span><span class="sxs-lookup"><span data-stu-id="4a74a-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="4a74a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a74a-118">PARAMETERS</span></span>

### <span data-ttu-id="4a74a-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a74a-119">-DatabaseName</span></span>
<span data-ttu-id="4a74a-120">Określa nazwę bazy danych SQL, dla której to polecenie cmdlet uzyskuje wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="4a74a-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="4a74a-121">Jeśli nie określisz bazy danych, to polecenie cmdlet pobiera wskazówki dla wszystkich baz danych na serwerze logicznym.</span><span class="sxs-lookup"><span data-stu-id="4a74a-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a74a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a74a-122">-DefaultProfile</span></span>
<span data-ttu-id="4a74a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4a74a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a74a-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="4a74a-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="4a74a-125">Wskazuje, czy bazy danych w elastycznych pulach baz danych są wykluczane z zwracanych rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="4a74a-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="4a74a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a74a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a74a-127">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4a74a-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4a74a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a74a-128">-ServerName</span></span>
<span data-ttu-id="4a74a-129">Określa nazwę serwera hostowego bazę danych, dla którego to polecenie cmdlet otrzymuje wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="4a74a-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="4a74a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a74a-130">-Confirm</span></span>
<span data-ttu-id="4a74a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4a74a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a74a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a74a-132">-WhatIf</span></span>
<span data-ttu-id="4a74a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a74a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a74a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4a74a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a74a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a74a-135">CommonParameters</span></span>
<span data-ttu-id="4a74a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a74a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a74a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a74a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a74a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a74a-138">INPUTS</span></span>

### <span data-ttu-id="4a74a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4a74a-139">System.String</span></span>

### <span data-ttu-id="4a74a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a74a-140">System.Boolean</span></span>

## <span data-ttu-id="4a74a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a74a-141">OUTPUTS</span></span>

### <span data-ttu-id="4a74a-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="4a74a-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="4a74a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a74a-143">NOTES</span></span>

## <span data-ttu-id="4a74a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a74a-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a74a-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="4a74a-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="4a74a-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="4a74a-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


