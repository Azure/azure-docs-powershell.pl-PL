---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241971"
---
# <span data-ttu-id="a8642-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a8642-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="a8642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8642-102">SYNOPSIS</span></span>
<span data-ttu-id="a8642-103">Pobiera usuniętą bazę danych, która można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="a8642-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="a8642-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8642-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8642-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8642-105">DESCRIPTION</span></span>
<span data-ttu-id="a8642-106">Polecenie **cmdlet Get-AzSqlDeletedDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych SQL, która można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="a8642-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="a8642-107">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a8642-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a8642-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8642-108">EXAMPLES</span></span>

### <span data-ttu-id="a8642-109">Przykład 1. Uzyskiwanie wszystkich usuniętych kopii zapasowych bazy danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="a8642-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="a8642-110">To polecenie pobiera wszystkie usunięte kopie zapasowe baz danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="a8642-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="a8642-111">Przykład 2. Uzyskiwanie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="a8642-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="a8642-112">To polecenie pobiera usuniętą kopię zapasową bazy danych dla bazy danych ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="a8642-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="a8642-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8642-113">PARAMETERS</span></span>

### <span data-ttu-id="a8642-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8642-114">-DatabaseName</span></span>
<span data-ttu-id="a8642-115">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a8642-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a8642-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8642-116">-DefaultProfile</span></span>
<span data-ttu-id="a8642-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a8642-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8642-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a8642-118">-DeletionDate</span></span>
<span data-ttu-id="a8642-119">Określa datę usunięcia bazy danych jako obiektu **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="a8642-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="a8642-120">Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8642-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a8642-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8642-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8642-122">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="a8642-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a8642-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8642-123">-ServerName</span></span>
<span data-ttu-id="a8642-124">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a8642-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="a8642-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8642-125">-Confirm</span></span>
<span data-ttu-id="a8642-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8642-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8642-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8642-127">-WhatIf</span></span>
<span data-ttu-id="a8642-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8642-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8642-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8642-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8642-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8642-130">CommonParameters</span></span>
<span data-ttu-id="a8642-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8642-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8642-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8642-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8642-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8642-133">INPUTS</span></span>

### <span data-ttu-id="a8642-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a8642-134">System.String</span></span>

### <span data-ttu-id="a8642-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8642-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a8642-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8642-136">OUTPUTS</span></span>

### <span data-ttu-id="a8642-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="a8642-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="a8642-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8642-138">NOTES</span></span>

## <span data-ttu-id="a8642-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8642-139">RELATED LINKS</span></span>

[<span data-ttu-id="a8642-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8642-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a8642-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a8642-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
