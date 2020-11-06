---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524818"
---
# <span data-ttu-id="68cae-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="68cae-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="68cae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68cae-102">SYNOPSIS</span></span>
<span data-ttu-id="68cae-103">Tworzy kopię bazy danych SQL, która w bieżącym czasie używa migawki.</span><span class="sxs-lookup"><span data-stu-id="68cae-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68cae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68cae-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68cae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68cae-105">DESCRIPTION</span></span>
<span data-ttu-id="68cae-106">Polecenie cmdlet **New-AzureRmSqlDatabaseCopy** tworzy kopię bazy danych SQL Azure używającej migawki danych w bieżącym czasie.</span><span class="sxs-lookup"><span data-stu-id="68cae-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="68cae-107">Użyj tego polecenia cmdlet zamiast polecenia cmdlet Start-AzureSqlDatabaseCopy, aby utworzyć jednorazową kopię bazy danych.</span><span class="sxs-lookup"><span data-stu-id="68cae-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="68cae-108">To polecenie cmdlet zwraca obiekt **bazy danych** kopii.</span><span class="sxs-lookup"><span data-stu-id="68cae-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="68cae-109">Uwaga: Użyj polecenia cmdlet New-AzureRmSqlDatabaseSecondary, aby skonfigurować replikację geograficzną dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="68cae-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="68cae-110">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="68cae-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="68cae-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68cae-111">EXAMPLES</span></span>

## <span data-ttu-id="68cae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68cae-112">PARAMETERS</span></span>

### <span data-ttu-id="68cae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68cae-113">-AsJob</span></span>
<span data-ttu-id="68cae-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="68cae-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="68cae-115">-CopyDatabaseName</span></span>
<span data-ttu-id="68cae-116">Określa nazwę kopii bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="68cae-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cae-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="68cae-118">Określa nazwę grupy zasobów platformy Azure, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="68cae-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="68cae-119">-CopyServerName</span></span>
<span data-ttu-id="68cae-120">Określa nazwę serwera SQL, na którym znajduje się kopia.</span><span class="sxs-lookup"><span data-stu-id="68cae-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68cae-121">-DatabaseName</span></span>
<span data-ttu-id="68cae-122">Określa nazwę bazy danych SQL do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="68cae-122">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="68cae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cae-123">-DefaultProfile</span></span>
<span data-ttu-id="68cae-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68cae-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68cae-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="68cae-125">-ElasticPoolName</span></span>
<span data-ttu-id="68cae-126">Określa nazwę puli elastycznej, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="68cae-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cae-127">-ResourceGroupName</span></span>
<span data-ttu-id="68cae-128">Określa nazwę grupy zasobów zawierającej bazę danych do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="68cae-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="68cae-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="68cae-129">-ServerName</span></span>
<span data-ttu-id="68cae-130">Określa nazwę serwera SQL zawierającego bazę danych do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="68cae-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="68cae-131">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="68cae-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="68cae-132">Określa nazwę celu usługi, który ma zostać przypisany do kopii.</span><span class="sxs-lookup"><span data-stu-id="68cae-132">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="68cae-133">-Tags</span></span>
<span data-ttu-id="68cae-134">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z kopią bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="68cae-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="68cae-135">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="68cae-135">For example:</span></span>

<span data-ttu-id="68cae-136">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="68cae-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68cae-137">-Confirm</span></span>
<span data-ttu-id="68cae-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68cae-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68cae-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cae-139">-WhatIf</span></span>
<span data-ttu-id="68cae-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68cae-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68cae-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68cae-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68cae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cae-142">CommonParameters</span></span>
<span data-ttu-id="68cae-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cae-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cae-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cae-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68cae-145">INPUTS</span></span>

### <span data-ttu-id="68cae-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="68cae-146">None</span></span>
<span data-ttu-id="68cae-147">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="68cae-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68cae-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68cae-148">OUTPUTS</span></span>

### <span data-ttu-id="68cae-149">Microsoft. Azure. Commands. SQL. Replication. model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="68cae-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="68cae-150">To polecenie cmdlet zwraca obiekt **bazy danych** reprezentujący skopiowaną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="68cae-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="68cae-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68cae-151">NOTES</span></span>

## <span data-ttu-id="68cae-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68cae-152">RELATED LINKS</span></span>

[<span data-ttu-id="68cae-153">Nowe — AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="68cae-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="68cae-154">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="68cae-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
