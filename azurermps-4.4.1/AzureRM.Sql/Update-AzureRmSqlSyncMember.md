---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717563"
---
# <span data-ttu-id="9a3f6-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9a3f6-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="9a3f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3f6-103">Umożliwia zaktualizowanie elementu członkowskiego synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a3f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a3f6-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a3f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="9a3f6-106">Polecenie cmdlet **Update-AzureRmSqlSyncGroup** modyfikuje właściwości członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="9a3f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="9a3f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a3f6-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="9a3f6-109">To polecenie resetuje hasło administratora bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="9a3f6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="9a3f6-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a3f6-111">-Confirm</span></span>
<span data-ttu-id="9a3f6-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a3f6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a3f6-113">-DatabaseName</span></span>
<span data-ttu-id="9a3f6-114">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9a3f6-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="9a3f6-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="9a3f6-116">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9a3f6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a3f6-117">-Name</span></span>
<span data-ttu-id="9a3f6-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-118">The sync member name.</span></span>

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

### <span data-ttu-id="9a3f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="9a3f6-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a3f6-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9a3f6-121">-ServerName</span></span>
<span data-ttu-id="9a3f6-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9a3f6-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3f6-123">-SyncGroupName</span></span>
<span data-ttu-id="9a3f6-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-124">The sync group name.</span></span>

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

### <span data-ttu-id="9a3f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a3f6-125">-WhatIf</span></span>
<span data-ttu-id="9a3f6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a3f6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a3f6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3f6-128">-DefaultProfile</span></span>
<span data-ttu-id="9a3f6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a3f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3f6-130">CommonParameters</span></span>
<span data-ttu-id="9a3f6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a3f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3f6-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3f6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3f6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a3f6-133">INPUTS</span></span>

## <span data-ttu-id="9a3f6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a3f6-134">OUTPUTS</span></span>

### <span data-ttu-id="9a3f6-135">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="9a3f6-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="9a3f6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a3f6-136">NOTES</span></span>

## <span data-ttu-id="9a3f6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a3f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="9a3f6-138">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9a3f6-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="9a3f6-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9a3f6-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="9a3f6-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9a3f6-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

