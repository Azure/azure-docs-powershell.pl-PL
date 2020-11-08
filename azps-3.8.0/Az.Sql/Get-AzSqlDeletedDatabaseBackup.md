---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050484"
---
# <span data-ttu-id="0e2e0-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0e2e0-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="0e2e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2e0-103">Pobieranie usuniętej bazy danych, którą można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="0e2e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e2e0-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e2e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e2e0-106">Polecenie cmdlet **Get-AzSqlDeletedDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych SQL, którą można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="0e2e0-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0e2e0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e2e0-108">EXAMPLES</span></span>

### <span data-ttu-id="0e2e0-109">Przykład 1: pobieranie wszystkich usuniętych kopii zapasowych baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="0e2e0-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="0e2e0-110">To polecenie pobiera wszystkie kopie zapasowe usunięte z bazy danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="0e2e0-111">Przykład 2: pobieranie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="0e2e0-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="0e2e0-112">To polecenie pobiera kopię zapasową usuniętej bazy danych dla ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="0e2e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e2e0-113">PARAMETERS</span></span>

### <span data-ttu-id="0e2e0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e2e0-114">-DatabaseName</span></span>
<span data-ttu-id="0e2e0-115">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0e2e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2e0-116">-DefaultProfile</span></span>
<span data-ttu-id="0e2e0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e2e0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e2e0-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0e2e0-118">-DeletionDate</span></span>
<span data-ttu-id="0e2e0-119">Określa datę, jako obiekt **DateTime** , że baza danych została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="0e2e0-120">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e2e0-122">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0e2e0-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0e2e0-123">-ServerName</span></span>
<span data-ttu-id="0e2e0-124">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="0e2e0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e2e0-125">-Confirm</span></span>
<span data-ttu-id="0e2e0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e2e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2e0-127">-WhatIf</span></span>
<span data-ttu-id="0e2e0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e2e0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e2e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2e0-130">CommonParameters</span></span>
<span data-ttu-id="0e2e0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2e0-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e2e0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2e0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e2e0-133">INPUTS</span></span>

### <span data-ttu-id="0e2e0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0e2e0-134">System.String</span></span>

### <span data-ttu-id="0e2e0-135">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e2e0-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0e2e0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e2e0-136">OUTPUTS</span></span>

### <span data-ttu-id="0e2e0-137">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="0e2e0-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="0e2e0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e2e0-138">NOTES</span></span>

## <span data-ttu-id="0e2e0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e2e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e2e0-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0e2e0-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0e2e0-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0e2e0-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
