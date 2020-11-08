---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049730"
---
# <span data-ttu-id="cc8fe-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="cc8fe-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="cc8fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8fe-103">Zwraca dzienniki grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="cc8fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc8fe-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc8fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="cc8fe-106">Polecenie cmdlet **Get-AzSqlSyncGroupLog** zwraca dzienniki grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="cc8fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc8fe-107">EXAMPLES</span></span>

### <span data-ttu-id="cc8fe-108">Przykład 1. Pobierz dzienniki grupy synchronizacji Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="cc8fe-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="cc8fe-109">To polecenie pobiera dzienniki grupy synchronizacji Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="cc8fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc8fe-110">PARAMETERS</span></span>

### <span data-ttu-id="cc8fe-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc8fe-111">-DatabaseName</span></span>
<span data-ttu-id="cc8fe-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="cc8fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8fe-113">-DefaultProfile</span></span>
<span data-ttu-id="cc8fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc8fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc8fe-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="cc8fe-115">-EndTime</span></span>
<span data-ttu-id="cc8fe-116">Godzina zakończenia dzienników do zbadania.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="cc8fe-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="cc8fe-117">-LogLevel</span></span>
<span data-ttu-id="cc8fe-118">Typ dzienników do zbadania.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-118">The type of the logs to query.</span></span>
<span data-ttu-id="cc8fe-119">Prawidłowe wartości: "Error", "Warning", "Success" i "All".</span><span class="sxs-lookup"><span data-stu-id="cc8fe-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="cc8fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc8fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="cc8fe-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc8fe-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cc8fe-122">-ServerName</span></span>
<span data-ttu-id="cc8fe-123">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="cc8fe-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cc8fe-124">-StartTime</span></span>
<span data-ttu-id="cc8fe-125">Godzina rozpoczęcia dziennika do zbadania.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="cc8fe-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="cc8fe-126">-SyncGroupName</span></span>
<span data-ttu-id="cc8fe-127">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-127">The sync group name.</span></span>

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

### <span data-ttu-id="cc8fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8fe-128">CommonParameters</span></span>
<span data-ttu-id="cc8fe-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc8fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8fe-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc8fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8fe-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc8fe-131">INPUTS</span></span>

### <span data-ttu-id="cc8fe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cc8fe-132">System.String</span></span>

## <span data-ttu-id="cc8fe-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc8fe-133">OUTPUTS</span></span>

### <span data-ttu-id="cc8fe-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="cc8fe-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="cc8fe-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc8fe-135">NOTES</span></span>

## <span data-ttu-id="cc8fe-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc8fe-136">RELATED LINKS</span></span>
