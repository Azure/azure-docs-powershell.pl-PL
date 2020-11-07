---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542191"
---
# <span data-ttu-id="77b07-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="77b07-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="77b07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77b07-102">SYNOPSIS</span></span>
<span data-ttu-id="77b07-103">Usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77b07-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77b07-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77b07-105">DESCRIPTION</span></span>
<span data-ttu-id="77b07-106">Polecenie cmdlet **Remove-AzureRmSqlSyncMember** usuwa członka synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77b07-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="77b07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77b07-107">EXAMPLES</span></span>

### <span data-ttu-id="77b07-108">Przykład 1. Usuń członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="77b07-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="77b07-109">To polecenie usuwa członka synchronizacji bazy danych SQL Azure o nazwie syncMember01.</span><span class="sxs-lookup"><span data-stu-id="77b07-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="77b07-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77b07-110">PARAMETERS</span></span>

### <span data-ttu-id="77b07-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77b07-111">-DatabaseName</span></span>
<span data-ttu-id="77b07-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="77b07-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="77b07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b07-113">-DefaultProfile</span></span>
<span data-ttu-id="77b07-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="77b07-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77b07-115">-Force</span></span>
<span data-ttu-id="77b07-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="77b07-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="77b07-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77b07-117">-Name</span></span>
<span data-ttu-id="77b07-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="77b07-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b07-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77b07-119">-PassThru</span></span>
<span data-ttu-id="77b07-120">Określa, czy zwrócić usunięty element synchronizacji</span><span class="sxs-lookup"><span data-stu-id="77b07-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="77b07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b07-121">-ResourceGroupName</span></span>
<span data-ttu-id="77b07-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77b07-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="77b07-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="77b07-123">-ServerName</span></span>
<span data-ttu-id="77b07-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77b07-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="77b07-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="77b07-125">-SyncGroupName</span></span>
<span data-ttu-id="77b07-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="77b07-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b07-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77b07-127">-Confirm</span></span>
<span data-ttu-id="77b07-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b07-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b07-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b07-129">-WhatIf</span></span>
<span data-ttu-id="77b07-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b07-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b07-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77b07-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b07-132">CommonParameters</span></span>
<span data-ttu-id="77b07-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b07-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b07-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b07-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77b07-135">INPUTS</span></span>

### <span data-ttu-id="77b07-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77b07-136">None</span></span>
<span data-ttu-id="77b07-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="77b07-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77b07-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77b07-138">OUTPUTS</span></span>

### <span data-ttu-id="77b07-139">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="77b07-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="77b07-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77b07-140">NOTES</span></span>

## <span data-ttu-id="77b07-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77b07-141">RELATED LINKS</span></span>

[<span data-ttu-id="77b07-142">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="77b07-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="77b07-143">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="77b07-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="77b07-144">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="77b07-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)
