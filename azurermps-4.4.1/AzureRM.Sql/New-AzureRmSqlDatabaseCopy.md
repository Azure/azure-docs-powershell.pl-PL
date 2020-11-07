---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719227"
---
# <span data-ttu-id="7f440-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7f440-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="7f440-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f440-102">SYNOPSIS</span></span>
<span data-ttu-id="7f440-103">Tworzy kopię bazy danych SQL, która w bieżącym czasie używa migawki.</span><span class="sxs-lookup"><span data-stu-id="7f440-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f440-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f440-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f440-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f440-105">DESCRIPTION</span></span>
<span data-ttu-id="7f440-106">Polecenie cmdlet **New-AzureRmSqlDatabaseCopy** tworzy kopię bazy danych SQL Azure używającej migawki danych w bieżącym czasie.</span><span class="sxs-lookup"><span data-stu-id="7f440-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="7f440-107">Użyj tego polecenia cmdlet zamiast polecenia cmdlet Start-AzureSqlDatabaseCopy, aby utworzyć jednorazową kopię bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7f440-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="7f440-108">To polecenie cmdlet zwraca obiekt **bazy danych** kopii.</span><span class="sxs-lookup"><span data-stu-id="7f440-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="7f440-109">Uwaga: Użyj polecenia cmdlet New-AzureRmSqlDatabaseSecondary, aby skonfigurować replikację geograficzną dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7f440-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="7f440-110">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7f440-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7f440-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f440-111">EXAMPLES</span></span>

## <span data-ttu-id="7f440-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f440-112">PARAMETERS</span></span>

### <span data-ttu-id="7f440-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f440-113">-CopyDatabaseName</span></span>
<span data-ttu-id="7f440-114">Określa nazwę kopii bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="7f440-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="7f440-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f440-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="7f440-116">Określa nazwę grupy zasobów platformy Azure, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="7f440-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="7f440-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="7f440-117">-CopyServerName</span></span>
<span data-ttu-id="7f440-118">Określa nazwę serwera SQL, na którym znajduje się kopia.</span><span class="sxs-lookup"><span data-stu-id="7f440-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="7f440-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f440-119">-DatabaseName</span></span>
<span data-ttu-id="7f440-120">Określa nazwę bazy danych SQL do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="7f440-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="7f440-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7f440-121">-ElasticPoolName</span></span>
<span data-ttu-id="7f440-122">Określa nazwę puli elastycznej, w której ma zostać przypisana kopia.</span><span class="sxs-lookup"><span data-stu-id="7f440-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="7f440-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f440-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f440-124">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje skopiowaną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7f440-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="7f440-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7f440-125">-ServerName</span></span>
<span data-ttu-id="7f440-126">Określa nazwę serwera SQL zawierającego bazę danych do skopiowania.</span><span class="sxs-lookup"><span data-stu-id="7f440-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="7f440-127">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="7f440-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="7f440-128">Określa nazwę celu usługi, który ma zostać przypisany do kopii.</span><span class="sxs-lookup"><span data-stu-id="7f440-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="7f440-129">-Tagi</span><span class="sxs-lookup"><span data-stu-id="7f440-129">-Tags</span></span>
<span data-ttu-id="7f440-130">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z kopią bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7f440-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="7f440-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7f440-131">For example:</span></span>

<span data-ttu-id="7f440-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7f440-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7f440-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f440-133">-Confirm</span></span>
<span data-ttu-id="7f440-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f440-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f440-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f440-135">-WhatIf</span></span>
<span data-ttu-id="7f440-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f440-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f440-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f440-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f440-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f440-138">-DefaultProfile</span></span>
<span data-ttu-id="7f440-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f440-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f440-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f440-140">CommonParameters</span></span>
<span data-ttu-id="7f440-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f440-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f440-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f440-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f440-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f440-143">INPUTS</span></span>

## <span data-ttu-id="7f440-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f440-144">OUTPUTS</span></span>

### <span data-ttu-id="7f440-145">Microsoft. Azure. Commands. SQL. Replication. model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="7f440-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="7f440-146">To polecenie cmdlet zwraca obiekt **bazy danych** reprezentujący skopiowaną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7f440-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="7f440-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f440-147">NOTES</span></span>

## <span data-ttu-id="7f440-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f440-148">RELATED LINKS</span></span>

[<span data-ttu-id="7f440-149">Nowe — AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7f440-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7f440-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7f440-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
