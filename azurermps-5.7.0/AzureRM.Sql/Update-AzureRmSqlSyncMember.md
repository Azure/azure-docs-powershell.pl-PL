---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: afaa0446b46fca343b4d53ae491c67ef1ceb923a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550491"
---
# <span data-ttu-id="79258-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="79258-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="79258-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79258-102">SYNOPSIS</span></span>
<span data-ttu-id="79258-103">Umożliwia zaktualizowanie elementu członkowskiego synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="79258-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79258-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79258-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79258-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79258-105">DESCRIPTION</span></span>
<span data-ttu-id="79258-106">Polecenie cmdlet **Update-AzureRmSqlSyncGroup** modyfikuje właściwości członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="79258-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="79258-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79258-107">EXAMPLES</span></span>

### <span data-ttu-id="79258-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79258-108">Example 1</span></span>
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

<span data-ttu-id="79258-109">To polecenie resetuje hasło administratora bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="79258-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="79258-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79258-110">PARAMETERS</span></span>

### <span data-ttu-id="79258-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79258-111">-DatabaseName</span></span>
<span data-ttu-id="79258-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="79258-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="79258-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79258-113">-DefaultProfile</span></span>
<span data-ttu-id="79258-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="79258-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79258-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="79258-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="79258-116">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="79258-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79258-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79258-117">-Name</span></span>
<span data-ttu-id="79258-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="79258-118">The sync member name.</span></span>

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

### <span data-ttu-id="79258-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79258-119">-ResourceGroupName</span></span>
<span data-ttu-id="79258-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79258-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="79258-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="79258-121">-ServerName</span></span>
<span data-ttu-id="79258-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79258-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="79258-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="79258-123">-SyncGroupName</span></span>
<span data-ttu-id="79258-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="79258-124">The sync group name.</span></span>

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

### <span data-ttu-id="79258-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79258-125">-Confirm</span></span>
<span data-ttu-id="79258-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79258-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79258-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79258-127">-WhatIf</span></span>
<span data-ttu-id="79258-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79258-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79258-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79258-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79258-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79258-130">CommonParameters</span></span>
<span data-ttu-id="79258-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79258-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79258-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79258-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79258-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79258-133">INPUTS</span></span>

### <span data-ttu-id="79258-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="79258-134">None</span></span>
<span data-ttu-id="79258-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="79258-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79258-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79258-136">OUTPUTS</span></span>

### <span data-ttu-id="79258-137">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="79258-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="79258-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79258-138">NOTES</span></span>

## <span data-ttu-id="79258-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79258-139">RELATED LINKS</span></span>

[<span data-ttu-id="79258-140">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="79258-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="79258-141">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="79258-141">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="79258-142">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="79258-142">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

