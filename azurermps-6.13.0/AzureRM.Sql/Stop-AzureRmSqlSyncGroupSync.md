---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 9cd213aea4e6211f52b076fca753385aefb1b449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543311"
---
# <span data-ttu-id="d10a6-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d10a6-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="d10a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d10a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d10a6-103">Zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d10a6-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d10a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d10a6-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d10a6-105">DESCRIPTION</span></span>
<span data-ttu-id="d10a6-106">Polecenie cmdlet **stop-AzureRmSqlSyncGroupSync** zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d10a6-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="d10a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d10a6-107">EXAMPLES</span></span>

### <span data-ttu-id="d10a6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d10a6-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="d10a6-109">To polecenie zatrzymuje synchronizację przeprowadzonej w odniesieniu do grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="d10a6-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="d10a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d10a6-110">PARAMETERS</span></span>

### <span data-ttu-id="d10a6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d10a6-111">-DatabaseName</span></span>
<span data-ttu-id="d10a6-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="d10a6-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d10a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10a6-113">-DefaultProfile</span></span>
<span data-ttu-id="d10a6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d10a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d10a6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d10a6-115">-PassThru</span></span>
<span data-ttu-id="d10a6-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d10a6-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="d10a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="d10a6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d10a6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d10a6-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d10a6-119">-ServerName</span></span>
<span data-ttu-id="d10a6-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d10a6-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d10a6-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d10a6-121">-SyncGroupName</span></span>
<span data-ttu-id="d10a6-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d10a6-122">The sync group name.</span></span>

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

### <span data-ttu-id="d10a6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d10a6-123">-Confirm</span></span>
<span data-ttu-id="d10a6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10a6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10a6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10a6-125">-WhatIf</span></span>
<span data-ttu-id="d10a6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10a6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d10a6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d10a6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10a6-128">CommonParameters</span></span>
<span data-ttu-id="d10a6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10a6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10a6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10a6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d10a6-131">INPUTS</span></span>

### <span data-ttu-id="d10a6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d10a6-132">System.String</span></span>

## <span data-ttu-id="d10a6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d10a6-133">OUTPUTS</span></span>

### <span data-ttu-id="d10a6-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d10a6-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d10a6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d10a6-135">NOTES</span></span>

## <span data-ttu-id="d10a6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d10a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d10a6-137">Start — AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d10a6-137">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

