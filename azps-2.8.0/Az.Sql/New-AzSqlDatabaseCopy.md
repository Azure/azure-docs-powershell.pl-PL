---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: aa2ba844e364d1c95274573a6b1b38e4550c70f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886866"
---
# <span data-ttu-id="5f972-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5f972-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="5f972-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f972-102">SYNOPSIS</span></span>
<span data-ttu-id="5f972-103">Tworzy kopię bazy danych SQL, która w bieżącym czasie używa migawki.</span><span class="sxs-lookup"><span data-stu-id="5f972-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="5f972-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f972-104">SYNTAX</span></span>

### <span data-ttu-id="5f972-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f972-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f972-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5f972-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f972-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5f972-107">DESCRIPTION</span></span>
<span data-ttu-id="5f972-108">Polecenie cmdlet **New-AzSqlDatabaseCopy** tworzy kopię bazy danych SQL Azure używającej migawki danych w bieżącym czasie.</span><span class="sxs-lookup"><span data-stu-id="5f972-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="5f972-109">Użyj tego polecenia cmdlet zamiast polecenia cmdlet Start-AzSqlDatabaseCopy, aby utworzyć jednorazową kopię bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5f972-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="5f972-110">To polecenie cmdlet zwraca obiekt **bazy danych** kopii.</span><span class="sxs-lookup"><span data-stu-id="5f972-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="5f972-111">Uwaga: Użyj polecenia cmdlet New-AzSqlDatabaseSecondary, aby skonfigurować replikację geograficzną dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5f972-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="5f972-112">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5f972-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5f972-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f972-113">EXAMPLES</span></span>

## <span data-ttu-id="5f972-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f972-114">PARAMETERS</span></span>

### <span data-ttu-id="5f972-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f972-115">-AsJob</span></span>
<span data-ttu-id="5f972-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5f972-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f972-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5f972-117">-ComputeGeneration</span></span>
<span data-ttu-id="5f972-118">Generowanie obliczeń w celu przypisania nowej kopii.</span><span class="sxs-lookup"><span data-stu-id="5f972-118">The compute generation to assign to the new copy.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f972-119">-CopyDatabaseName</span></span>
<span data-ttu-id="5f972-120">Określa nazwę kopii bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f972-120">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f972-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="5f972-122">Określa nazwę grupy zasobów platformy Azure, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="5f972-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="5f972-123">-CopyServerName</span></span>
<span data-ttu-id="5f972-124">Określa nazwę serwera SQL, na którym znajduje się kopia.</span><span class="sxs-lookup"><span data-stu-id="5f972-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f972-125">-DatabaseName</span></span>
<span data-ttu-id="5f972-126">Określa nazwę bazy danych SQL do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="5f972-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="5f972-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f972-127">-DefaultProfile</span></span>
<span data-ttu-id="5f972-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5f972-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f972-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5f972-129">-ElasticPoolName</span></span>
<span data-ttu-id="5f972-130">Określa nazwę puli elastycznej, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="5f972-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5f972-131">-LicenseType</span></span>
<span data-ttu-id="5f972-132">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5f972-132">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f972-133">-ResourceGroupName</span></span>
<span data-ttu-id="5f972-134">Określa nazwę grupy zasobów zawierającej bazę danych do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="5f972-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="5f972-135">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5f972-135">-ServerName</span></span>
<span data-ttu-id="5f972-136">Określa nazwę serwera SQL zawierającego bazę danych do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="5f972-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="5f972-137">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="5f972-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="5f972-138">Określa nazwę celu usługi, który ma zostać przypisany do kopii.</span><span class="sxs-lookup"><span data-stu-id="5f972-138">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-139">-Tagi</span><span class="sxs-lookup"><span data-stu-id="5f972-139">-Tags</span></span>
<span data-ttu-id="5f972-140">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z kopią bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5f972-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="5f972-141">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5f972-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="5f972-142">-VCore</span></span>
<span data-ttu-id="5f972-143">Numery vCore kopii bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5f972-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f972-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f972-144">-Confirm</span></span>
<span data-ttu-id="5f972-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f972-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f972-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f972-146">-WhatIf</span></span>
<span data-ttu-id="5f972-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f972-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f972-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f972-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f972-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f972-149">CommonParameters</span></span>
<span data-ttu-id="5f972-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f972-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f972-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f972-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f972-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f972-152">INPUTS</span></span>

### <span data-ttu-id="5f972-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5f972-153">System.String</span></span>

## <span data-ttu-id="5f972-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f972-154">OUTPUTS</span></span>

### <span data-ttu-id="5f972-155">Microsoft. Azure. Commands. SQL. Replication. model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="5f972-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="5f972-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f972-156">NOTES</span></span>

## <span data-ttu-id="5f972-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f972-157">RELATED LINKS</span></span>

[<span data-ttu-id="5f972-158">Nowe — AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5f972-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="5f972-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5f972-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)