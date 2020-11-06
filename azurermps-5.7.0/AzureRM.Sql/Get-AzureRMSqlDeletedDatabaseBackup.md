---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524881"
---
# <span data-ttu-id="68f86-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="68f86-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="68f86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68f86-102">SYNOPSIS</span></span>
<span data-ttu-id="68f86-103">Pobieranie usuniętej bazy danych, którą można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="68f86-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68f86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68f86-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68f86-105">DESCRIPTION</span></span>
<span data-ttu-id="68f86-106">Polecenie cmdlet **Get-AzureRMSqlDeletedDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych SQL, którą można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="68f86-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="68f86-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="68f86-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="68f86-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68f86-108">EXAMPLES</span></span>

### <span data-ttu-id="68f86-109">Przykład 1: pobieranie wszystkich usuniętych kopii zapasowych baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="68f86-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="68f86-110">To polecenie pobiera wszystkie kopie zapasowe usunięte z bazy danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="68f86-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="68f86-111">Przykład 2: pobieranie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="68f86-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="68f86-112">To polecenie pobiera kopię zapasową usuniętej bazy danych dla ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="68f86-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="68f86-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68f86-113">PARAMETERS</span></span>

### <span data-ttu-id="68f86-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68f86-114">-DatabaseName</span></span>
<span data-ttu-id="68f86-115">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="68f86-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f86-116">-DefaultProfile</span></span>
<span data-ttu-id="68f86-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68f86-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68f86-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="68f86-118">-DeletionDate</span></span>
<span data-ttu-id="68f86-119">Określa datę, jako obiekt **DateTime** , że baza danych została usunięta.</span><span class="sxs-lookup"><span data-stu-id="68f86-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="68f86-120">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="68f86-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f86-121">-ResourceGroupName</span></span>
<span data-ttu-id="68f86-122">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="68f86-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="68f86-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="68f86-123">-ServerName</span></span>
<span data-ttu-id="68f86-124">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="68f86-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="68f86-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68f86-125">-Confirm</span></span>
<span data-ttu-id="68f86-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f86-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f86-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f86-127">-WhatIf</span></span>
<span data-ttu-id="68f86-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f86-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f86-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68f86-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f86-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f86-130">CommonParameters</span></span>
<span data-ttu-id="68f86-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f86-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f86-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f86-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f86-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68f86-133">INPUTS</span></span>

### <span data-ttu-id="68f86-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="68f86-134">None</span></span>
<span data-ttu-id="68f86-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="68f86-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68f86-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68f86-136">OUTPUTS</span></span>

## <span data-ttu-id="68f86-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68f86-137">NOTES</span></span>

## <span data-ttu-id="68f86-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68f86-138">RELATED LINKS</span></span>

[<span data-ttu-id="68f86-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="68f86-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="68f86-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="68f86-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
