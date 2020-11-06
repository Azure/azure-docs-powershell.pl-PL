---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544052"
---
# <span data-ttu-id="ba5d1-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ba5d1-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="ba5d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5d1-103">Rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba5d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba5d1-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba5d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5d1-106">Polecenie cmdlet **Start-AzureRmSqlSyncGroupSync** rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="ba5d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba5d1-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5d1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba5d1-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="ba5d1-109">To polecenie rozpoczyna rundę synchronizacji dla grupy synchronizacji mysg.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="ba5d1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba5d1-110">PARAMETERS</span></span>

### <span data-ttu-id="ba5d1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba5d1-111">-DatabaseName</span></span>
<span data-ttu-id="ba5d1-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5d1-113">-DefaultProfile</span></span>
<span data-ttu-id="ba5d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ba5d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba5d1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba5d1-115">-PassThru</span></span>
<span data-ttu-id="ba5d1-116">Określa, czy ma być zwracana Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="ba5d1-116">Defines Whether return the sync group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba5d1-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba5d1-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba5d1-119">-ServerName</span></span>
<span data-ttu-id="ba5d1-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ba5d1-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5d1-121">-SyncGroupName</span></span>
<span data-ttu-id="ba5d1-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5d1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba5d1-123">-Confirm</span></span>
<span data-ttu-id="ba5d1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5d1-125">-WhatIf</span></span>
<span data-ttu-id="ba5d1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5d1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5d1-128">CommonParameters</span></span>
<span data-ttu-id="ba5d1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5d1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5d1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba5d1-131">INPUTS</span></span>

### <span data-ttu-id="ba5d1-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ba5d1-132">None</span></span>
<span data-ttu-id="ba5d1-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ba5d1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba5d1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba5d1-134">OUTPUTS</span></span>

### <span data-ttu-id="ba5d1-135">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ba5d1-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ba5d1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba5d1-136">NOTES</span></span>

## <span data-ttu-id="ba5d1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba5d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba5d1-138">Zatrzymaj — AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ba5d1-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

