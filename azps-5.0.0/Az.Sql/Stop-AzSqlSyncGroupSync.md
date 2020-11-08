---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232753"
---
# <span data-ttu-id="274f2-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="274f2-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="274f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="274f2-102">SYNOPSIS</span></span>
<span data-ttu-id="274f2-103">Zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="274f2-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="274f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="274f2-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="274f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="274f2-105">DESCRIPTION</span></span>
<span data-ttu-id="274f2-106">Polecenie cmdlet **stop-AzSqlSyncGroupSync** zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="274f2-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="274f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="274f2-107">EXAMPLES</span></span>

### <span data-ttu-id="274f2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="274f2-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="274f2-109">To polecenie zatrzymuje synchronizację przeprowadzonej w odniesieniu do grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="274f2-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="274f2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="274f2-110">PARAMETERS</span></span>

### <span data-ttu-id="274f2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="274f2-111">-DatabaseName</span></span>
<span data-ttu-id="274f2-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="274f2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="274f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274f2-113">-DefaultProfile</span></span>
<span data-ttu-id="274f2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="274f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="274f2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="274f2-115">-PassThru</span></span>
<span data-ttu-id="274f2-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="274f2-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="274f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="274f2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="274f2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="274f2-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="274f2-119">-ServerName</span></span>
<span data-ttu-id="274f2-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="274f2-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="274f2-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="274f2-121">-SyncGroupName</span></span>
<span data-ttu-id="274f2-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="274f2-122">The sync group name.</span></span>

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

### <span data-ttu-id="274f2-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="274f2-123">-Confirm</span></span>
<span data-ttu-id="274f2-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="274f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="274f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="274f2-125">-WhatIf</span></span>
<span data-ttu-id="274f2-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="274f2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="274f2-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="274f2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="274f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274f2-128">CommonParameters</span></span>
<span data-ttu-id="274f2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274f2-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="274f2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274f2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="274f2-131">INPUTS</span></span>

### <span data-ttu-id="274f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="274f2-132">System.String</span></span>

## <span data-ttu-id="274f2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="274f2-133">OUTPUTS</span></span>

### <span data-ttu-id="274f2-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="274f2-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="274f2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="274f2-135">NOTES</span></span>

## <span data-ttu-id="274f2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="274f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="274f2-137">Start — AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="274f2-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

