---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: 5ef51d83cf2b4cc43693da1697ee15620db04ff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546403"
---
# <span data-ttu-id="2ad3c-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2ad3c-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="2ad3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ad3c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad3c-103">Usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ad3c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ad3c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad3c-106">Polecenie cmdlet **Remove-AzureRmSqlSyncMember** usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2ad3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ad3c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ad3c-108">Przykład 1. Usuń członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="2ad3c-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="2ad3c-109">To polecenie usuwa członka synchronizacji bazy danych SQL Azure o nazwie syncMember01.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="2ad3c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ad3c-110">PARAMETERS</span></span>

### <span data-ttu-id="2ad3c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ad3c-111">-DatabaseName</span></span>
<span data-ttu-id="2ad3c-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2ad3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad3c-113">-DefaultProfile</span></span>
<span data-ttu-id="2ad3c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2ad3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ad3c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ad3c-115">-Force</span></span>
<span data-ttu-id="2ad3c-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="2ad3c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2ad3c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ad3c-117">-Name</span></span>
<span data-ttu-id="2ad3c-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad3c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ad3c-119">-PassThru</span></span>
<span data-ttu-id="2ad3c-120">Określa, czy zwrócić usunięty element synchronizacji</span><span class="sxs-lookup"><span data-stu-id="2ad3c-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="2ad3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ad3c-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ad3c-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2ad3c-123">-ServerName</span></span>
<span data-ttu-id="2ad3c-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2ad3c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad3c-125">-SyncGroupName</span></span>
<span data-ttu-id="2ad3c-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad3c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ad3c-127">-Confirm</span></span>
<span data-ttu-id="2ad3c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad3c-129">-WhatIf</span></span>
<span data-ttu-id="2ad3c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad3c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad3c-132">CommonParameters</span></span>
<span data-ttu-id="2ad3c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad3c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad3c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad3c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ad3c-135">INPUTS</span></span>

### <span data-ttu-id="2ad3c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad3c-136">System.String</span></span>

## <span data-ttu-id="2ad3c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ad3c-137">OUTPUTS</span></span>

### <span data-ttu-id="2ad3c-138">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="2ad3c-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="2ad3c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ad3c-139">NOTES</span></span>

## <span data-ttu-id="2ad3c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ad3c-140">RELATED LINKS</span></span>

[<span data-ttu-id="2ad3c-141">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2ad3c-141">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="2ad3c-142">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2ad3c-142">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="2ad3c-143">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2ad3c-143">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

