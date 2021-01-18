---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499734"
---
# <span data-ttu-id="49e3a-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="49e3a-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="49e3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="49e3a-103">Umożliwia zaktualizowanie elementu członkowskiego synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="49e3a-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="49e3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49e3a-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49e3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="49e3a-106">Polecenie cmdlet **Update-AzSqlSyncGroup** modyfikuje właściwości członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="49e3a-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="49e3a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="49e3a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49e3a-108">Example 1</span></span>
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

<span data-ttu-id="49e3a-109">To polecenie resetuje hasło administratora bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="49e3a-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="49e3a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49e3a-110">PARAMETERS</span></span>

### <span data-ttu-id="49e3a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49e3a-111">-DatabaseName</span></span>
<span data-ttu-id="49e3a-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="49e3a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="49e3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e3a-113">-DefaultProfile</span></span>
<span data-ttu-id="49e3a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="49e3a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49e3a-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="49e3a-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="49e3a-116">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49e3a-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49e3a-117">-Name</span></span>
<span data-ttu-id="49e3a-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="49e3a-118">The sync member name.</span></span>

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

### <span data-ttu-id="49e3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="49e3a-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49e3a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="49e3a-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="49e3a-121">-ServerName</span></span>
<span data-ttu-id="49e3a-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="49e3a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="49e3a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="49e3a-123">-SyncGroupName</span></span>
<span data-ttu-id="49e3a-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="49e3a-124">The sync group name.</span></span>

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

### <span data-ttu-id="49e3a-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="49e3a-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="49e3a-126">Identyfikator zasobu dla bazy danych elementu członkowskiego synchronizacji, używana, jeśli UsePrivateLinkConnection ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="49e3a-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="49e3a-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="49e3a-128">Czy używać linku prywatnego podczas nawiązywania połączenia z tym członkiem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="49e3a-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49e3a-129">-Confirm</span></span>
<span data-ttu-id="49e3a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49e3a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e3a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e3a-131">-WhatIf</span></span>
<span data-ttu-id="49e3a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49e3a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49e3a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49e3a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e3a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e3a-134">CommonParameters</span></span>
<span data-ttu-id="49e3a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e3a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e3a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49e3a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e3a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e3a-137">INPUTS</span></span>

### <span data-ttu-id="49e3a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="49e3a-138">System.String</span></span>

## <span data-ttu-id="49e3a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49e3a-139">OUTPUTS</span></span>

### <span data-ttu-id="49e3a-140">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="49e3a-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="49e3a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49e3a-141">NOTES</span></span>

## <span data-ttu-id="49e3a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49e3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="49e3a-143">Nowe — AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="49e3a-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="49e3a-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="49e3a-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="49e3a-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="49e3a-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

