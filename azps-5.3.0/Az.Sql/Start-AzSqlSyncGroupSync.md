---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499757"
---
# <span data-ttu-id="d4531-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d4531-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="d4531-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4531-102">SYNOPSIS</span></span>
<span data-ttu-id="d4531-103">Rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4531-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="d4531-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4531-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4531-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4531-105">DESCRIPTION</span></span>
<span data-ttu-id="d4531-106">Polecenie cmdlet **Start-AzSqlSyncGroupSync** rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4531-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="d4531-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4531-107">EXAMPLES</span></span>

### <span data-ttu-id="d4531-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4531-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="d4531-109">To polecenie rozpoczyna rundę synchronizacji dla grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="d4531-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="d4531-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4531-110">PARAMETERS</span></span>

### <span data-ttu-id="d4531-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4531-111">-DatabaseName</span></span>
<span data-ttu-id="d4531-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="d4531-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d4531-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4531-113">-DefaultProfile</span></span>
<span data-ttu-id="d4531-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4531-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4531-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4531-115">-PassThru</span></span>
<span data-ttu-id="d4531-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d4531-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="d4531-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4531-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4531-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4531-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4531-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d4531-119">-ServerName</span></span>
<span data-ttu-id="d4531-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d4531-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d4531-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d4531-121">-SyncGroupName</span></span>
<span data-ttu-id="d4531-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4531-122">The sync group name.</span></span>

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

### <span data-ttu-id="d4531-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4531-123">-Confirm</span></span>
<span data-ttu-id="d4531-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4531-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4531-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4531-125">-WhatIf</span></span>
<span data-ttu-id="d4531-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4531-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4531-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4531-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4531-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4531-128">CommonParameters</span></span>
<span data-ttu-id="d4531-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4531-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4531-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4531-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4531-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4531-131">INPUTS</span></span>

### <span data-ttu-id="d4531-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d4531-132">System.String</span></span>

## <span data-ttu-id="d4531-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4531-133">OUTPUTS</span></span>

### <span data-ttu-id="d4531-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d4531-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d4531-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4531-135">NOTES</span></span>

## <span data-ttu-id="d4531-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4531-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4531-137">Zatrzymaj — AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d4531-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

