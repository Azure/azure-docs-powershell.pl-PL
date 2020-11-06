---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: d57e73c71e95fe673f9b54d9129714ca22670d31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554182"
---
# <span data-ttu-id="cafd2-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="cafd2-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="cafd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cafd2-102">SYNOPSIS</span></span>
<span data-ttu-id="cafd2-103">Usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cafd2-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cafd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cafd2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafd2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cafd2-105">DESCRIPTION</span></span>
<span data-ttu-id="cafd2-106">Polecenie cmdlet **Remove-AzureRmSqlSyncMember** usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cafd2-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="cafd2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cafd2-107">EXAMPLES</span></span>

### <span data-ttu-id="cafd2-108">Przykład 1. Usuń członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="cafd2-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="cafd2-109">To polecenie usuwa członka synchronizacji bazy danych SQL Azure o nazwie syncMember01.</span><span class="sxs-lookup"><span data-stu-id="cafd2-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="cafd2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cafd2-110">PARAMETERS</span></span>

### <span data-ttu-id="cafd2-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cafd2-111">-Confirm</span></span>
<span data-ttu-id="cafd2-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafd2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafd2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cafd2-113">-DatabaseName</span></span>
<span data-ttu-id="cafd2-114">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="cafd2-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="cafd2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cafd2-115">-Force</span></span>
<span data-ttu-id="cafd2-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="cafd2-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cafd2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cafd2-117">-Name</span></span>
<span data-ttu-id="cafd2-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cafd2-118">The sync member name.</span></span>

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

### <span data-ttu-id="cafd2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cafd2-119">-PassThru</span></span>
<span data-ttu-id="cafd2-120">Określa, czy zwrócić usunięty element synchronizacji</span><span class="sxs-lookup"><span data-stu-id="cafd2-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="cafd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="cafd2-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cafd2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="cafd2-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cafd2-123">-ServerName</span></span>
<span data-ttu-id="cafd2-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cafd2-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="cafd2-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="cafd2-125">-SyncGroupName</span></span>
<span data-ttu-id="cafd2-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cafd2-126">The sync group name.</span></span>

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

### <span data-ttu-id="cafd2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafd2-127">-WhatIf</span></span>
<span data-ttu-id="cafd2-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafd2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafd2-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cafd2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafd2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafd2-130">-DefaultProfile</span></span>
<span data-ttu-id="cafd2-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cafd2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cafd2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafd2-132">CommonParameters</span></span>
<span data-ttu-id="cafd2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cafd2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafd2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cafd2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafd2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cafd2-135">INPUTS</span></span>

## <span data-ttu-id="cafd2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cafd2-136">OUTPUTS</span></span>

### <span data-ttu-id="cafd2-137">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="cafd2-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="cafd2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cafd2-138">NOTES</span></span>

## <span data-ttu-id="cafd2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cafd2-139">RELATED LINKS</span></span>

[<span data-ttu-id="cafd2-140">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="cafd2-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="cafd2-141">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="cafd2-141">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="cafd2-142">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="cafd2-142">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

