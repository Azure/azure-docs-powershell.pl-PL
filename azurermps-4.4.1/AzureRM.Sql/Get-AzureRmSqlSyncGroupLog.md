---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527229"
---
# <span data-ttu-id="366ac-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="366ac-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="366ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="366ac-102">SYNOPSIS</span></span>
<span data-ttu-id="366ac-103">Zwraca dzienniki grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="366ac-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="366ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="366ac-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="366ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="366ac-105">DESCRIPTION</span></span>
<span data-ttu-id="366ac-106">Polecenie cmdlet **Get-AzureRmSqlSyncGroupLog** zwraca dzienniki grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="366ac-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="366ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="366ac-107">EXAMPLES</span></span>

### <span data-ttu-id="366ac-108">Przykład 1. Pobierz dzienniki grupy synchronizacji Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="366ac-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="366ac-109">To polecenie pobiera dzienniki grupy synchronizacji Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="366ac-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="366ac-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="366ac-110">PARAMETERS</span></span>

### <span data-ttu-id="366ac-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="366ac-111">-DatabaseName</span></span>
<span data-ttu-id="366ac-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="366ac-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="366ac-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="366ac-113">-EndTime</span></span>
<span data-ttu-id="366ac-114">Godzina zakończenia dzienników do zbadania.</span><span class="sxs-lookup"><span data-stu-id="366ac-114">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ac-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="366ac-115">-LogLevel</span></span>
<span data-ttu-id="366ac-116">Typ dzienników do zbadania.</span><span class="sxs-lookup"><span data-stu-id="366ac-116">The type of the logs to query.</span></span>
<span data-ttu-id="366ac-117">Prawidłowe wartości: "Error", "Warning", "Success" i "All".</span><span class="sxs-lookup"><span data-stu-id="366ac-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ac-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="366ac-118">-SyncGroupName</span></span>
<span data-ttu-id="366ac-119">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="366ac-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="366ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="366ac-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="366ac-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="366ac-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="366ac-122">-ServerName</span></span>
<span data-ttu-id="366ac-123">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="366ac-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="366ac-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="366ac-124">-StartTime</span></span>
<span data-ttu-id="366ac-125">Godzina rozpoczęcia dziennika do zbadania.</span><span class="sxs-lookup"><span data-stu-id="366ac-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366ac-126">-DefaultProfile</span></span>
<span data-ttu-id="366ac-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="366ac-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="366ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366ac-128">CommonParameters</span></span>
<span data-ttu-id="366ac-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366ac-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366ac-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="366ac-131">INPUTS</span></span>

## <span data-ttu-id="366ac-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="366ac-132">OUTPUTS</span></span>

### <span data-ttu-id="366ac-133">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="366ac-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="366ac-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="366ac-134">NOTES</span></span>

## <span data-ttu-id="366ac-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="366ac-135">RELATED LINKS</span></span>

