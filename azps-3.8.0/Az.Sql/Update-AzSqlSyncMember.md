---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895586"
---
# <span data-ttu-id="6e008-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e008-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="6e008-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e008-102">SYNOPSIS</span></span>
<span data-ttu-id="6e008-103">Umożliwia zaktualizowanie elementu członkowskiego synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6e008-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6e008-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e008-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e008-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e008-105">DESCRIPTION</span></span>
<span data-ttu-id="6e008-106">Polecenie cmdlet **Update-AzSqlSyncGroup** modyfikuje właściwości członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6e008-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6e008-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e008-107">EXAMPLES</span></span>

### <span data-ttu-id="6e008-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e008-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="6e008-109">To polecenie resetuje hasło administratora bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="6e008-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="6e008-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e008-110">PARAMETERS</span></span>

### <span data-ttu-id="6e008-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e008-111">-DatabaseName</span></span>
<span data-ttu-id="6e008-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="6e008-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6e008-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e008-113">-DefaultProfile</span></span>
<span data-ttu-id="6e008-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6e008-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e008-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6e008-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="6e008-116">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6e008-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e008-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e008-117">-Name</span></span>
<span data-ttu-id="6e008-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="6e008-118">The sync member name.</span></span>

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

### <span data-ttu-id="6e008-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e008-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e008-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e008-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e008-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6e008-121">-ServerName</span></span>
<span data-ttu-id="6e008-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e008-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6e008-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6e008-123">-SyncGroupName</span></span>
<span data-ttu-id="6e008-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="6e008-124">The sync group name.</span></span>

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

### <span data-ttu-id="6e008-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e008-125">-Confirm</span></span>
<span data-ttu-id="6e008-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e008-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e008-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e008-127">-WhatIf</span></span>
<span data-ttu-id="6e008-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e008-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e008-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e008-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e008-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e008-130">CommonParameters</span></span>
<span data-ttu-id="6e008-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e008-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e008-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e008-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e008-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e008-133">INPUTS</span></span>

### <span data-ttu-id="6e008-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6e008-134">System.String</span></span>

## <span data-ttu-id="6e008-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e008-135">OUTPUTS</span></span>

### <span data-ttu-id="6e008-136">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="6e008-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6e008-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e008-137">NOTES</span></span>

## <span data-ttu-id="6e008-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e008-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e008-139">Nowe — AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e008-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="6e008-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e008-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="6e008-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e008-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

