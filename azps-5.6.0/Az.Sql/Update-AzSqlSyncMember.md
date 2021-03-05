---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 3c4b50a4d4f4c01365d853e64cb3a53ea9c05d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992258"
---
# <span data-ttu-id="032fe-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="032fe-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="032fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="032fe-102">SYNOPSIS</span></span>
<span data-ttu-id="032fe-103">Aktualizuje członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="032fe-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="032fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="032fe-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="032fe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="032fe-105">DESCRIPTION</span></span>
<span data-ttu-id="032fe-106">Polecenie **cmdlet Update-AzSqlSyncGroup** modyfikuje właściwości członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="032fe-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="032fe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="032fe-107">EXAMPLES</span></span>

### <span data-ttu-id="032fe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="032fe-108">Example 1</span></span>
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

<span data-ttu-id="032fe-109">To polecenie powoduje zresetowanie hasła administratora bazy danych członków.</span><span class="sxs-lookup"><span data-stu-id="032fe-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="032fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="032fe-110">PARAMETERS</span></span>

### <span data-ttu-id="032fe-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="032fe-111">-DatabaseName</span></span>
<span data-ttu-id="032fe-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="032fe-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="032fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032fe-113">-DefaultProfile</span></span>
<span data-ttu-id="032fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="032fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="032fe-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="032fe-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="032fe-116">Poświadczenia (nazwa użytkownika i hasło) bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="032fe-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="032fe-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="032fe-117">-Name</span></span>
<span data-ttu-id="032fe-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="032fe-118">The sync member name.</span></span>

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

### <span data-ttu-id="032fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="032fe-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="032fe-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="032fe-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="032fe-121">-ServerName</span></span>
<span data-ttu-id="032fe-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="032fe-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="032fe-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="032fe-123">-SyncGroupName</span></span>
<span data-ttu-id="032fe-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="032fe-124">The sync group name.</span></span>

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

### <span data-ttu-id="032fe-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="032fe-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="032fe-126">Identyfikator zasobu dla bazy danych członka synchronizacji, używany w przypadku ustawienia UsePrivateLinkConnection na wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="032fe-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="032fe-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="032fe-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="032fe-128">Czy użyć linku prywatnego podczas łączenia się z tym członkiem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="032fe-128">Whether to use private link when connecting to this sync member.</span></span>

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

### <span data-ttu-id="032fe-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="032fe-129">-Confirm</span></span>
<span data-ttu-id="032fe-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="032fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032fe-131">-WhatIf</span></span>
<span data-ttu-id="032fe-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="032fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="032fe-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="032fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032fe-134">CommonParameters</span></span>
<span data-ttu-id="032fe-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="032fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032fe-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="032fe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032fe-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="032fe-137">INPUTS</span></span>

### <span data-ttu-id="032fe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="032fe-138">System.String</span></span>

## <span data-ttu-id="032fe-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="032fe-139">OUTPUTS</span></span>

### <span data-ttu-id="032fe-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="032fe-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="032fe-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="032fe-141">NOTES</span></span>

## <span data-ttu-id="032fe-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="032fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="032fe-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="032fe-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="032fe-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="032fe-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="032fe-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="032fe-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

