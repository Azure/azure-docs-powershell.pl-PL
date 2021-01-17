---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330469"
---
# <span data-ttu-id="c9334-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c9334-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="c9334-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9334-102">SYNOPSIS</span></span>
<span data-ttu-id="c9334-103">Zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c9334-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="c9334-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9334-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9334-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9334-105">DESCRIPTION</span></span>
<span data-ttu-id="c9334-106">Polecenie cmdlet **stop-AzSqlSyncGroupSync** zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c9334-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="c9334-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9334-107">EXAMPLES</span></span>

### <span data-ttu-id="c9334-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9334-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="c9334-109">To polecenie zatrzymuje synchronizację przeprowadzonej w odniesieniu do grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="c9334-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="c9334-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9334-110">PARAMETERS</span></span>

### <span data-ttu-id="c9334-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9334-111">-DatabaseName</span></span>
<span data-ttu-id="c9334-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="c9334-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c9334-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9334-113">-DefaultProfile</span></span>
<span data-ttu-id="c9334-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9334-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9334-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9334-115">-PassThru</span></span>
<span data-ttu-id="c9334-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="c9334-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="c9334-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9334-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9334-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9334-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9334-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c9334-119">-ServerName</span></span>
<span data-ttu-id="c9334-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9334-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c9334-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c9334-121">-SyncGroupName</span></span>
<span data-ttu-id="c9334-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c9334-122">The sync group name.</span></span>

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

### <span data-ttu-id="c9334-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9334-123">-Confirm</span></span>
<span data-ttu-id="c9334-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9334-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9334-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9334-125">-WhatIf</span></span>
<span data-ttu-id="c9334-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9334-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9334-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9334-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9334-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9334-128">CommonParameters</span></span>
<span data-ttu-id="c9334-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9334-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9334-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9334-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9334-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9334-131">INPUTS</span></span>

### <span data-ttu-id="c9334-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9334-132">System.String</span></span>

## <span data-ttu-id="c9334-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9334-133">OUTPUTS</span></span>

### <span data-ttu-id="c9334-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c9334-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c9334-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9334-135">NOTES</span></span>

## <span data-ttu-id="c9334-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9334-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9334-137">Start — AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c9334-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

