---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 6e6f0279f8cf3e0ea4481e31b06c42c25d0a0180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707699"
---
# <span data-ttu-id="d08eb-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d08eb-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="d08eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d08eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d08eb-103">Rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d08eb-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="d08eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d08eb-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d08eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d08eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d08eb-106">Polecenie cmdlet **Start-AzSqlSyncGroupSync** rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d08eb-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="d08eb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d08eb-107">EXAMPLES</span></span>

### <span data-ttu-id="d08eb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d08eb-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="d08eb-109">To polecenie rozpoczyna rundę synchronizacji dla grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="d08eb-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="d08eb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d08eb-110">PARAMETERS</span></span>

### <span data-ttu-id="d08eb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d08eb-111">-DatabaseName</span></span>
<span data-ttu-id="d08eb-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="d08eb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d08eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08eb-113">-DefaultProfile</span></span>
<span data-ttu-id="d08eb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d08eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d08eb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d08eb-115">-PassThru</span></span>
<span data-ttu-id="d08eb-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d08eb-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="d08eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d08eb-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d08eb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d08eb-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d08eb-119">-ServerName</span></span>
<span data-ttu-id="d08eb-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d08eb-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d08eb-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d08eb-121">-SyncGroupName</span></span>
<span data-ttu-id="d08eb-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d08eb-122">The sync group name.</span></span>

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

### <span data-ttu-id="d08eb-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d08eb-123">-Confirm</span></span>
<span data-ttu-id="d08eb-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d08eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d08eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d08eb-125">-WhatIf</span></span>
<span data-ttu-id="d08eb-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d08eb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d08eb-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d08eb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d08eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08eb-128">CommonParameters</span></span>
<span data-ttu-id="d08eb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08eb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d08eb-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08eb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d08eb-131">INPUTS</span></span>

### <span data-ttu-id="d08eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d08eb-132">System.String</span></span>

## <span data-ttu-id="d08eb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d08eb-133">OUTPUTS</span></span>

### <span data-ttu-id="d08eb-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d08eb-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d08eb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d08eb-135">NOTES</span></span>

## <span data-ttu-id="d08eb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d08eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="d08eb-137">Zatrzymaj — AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d08eb-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)
