---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318355"
---
# <span data-ttu-id="fbf2c-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="fbf2c-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="fbf2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf2c-103">Aktualizowanie schematu synchronizowania bazy danych członka synchronizacji lub bazy danych Centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="fbf2c-104">Pobierze on najnowszą wersję schematu bazy danych z rzeczywistej bazy danych, a następnie użyje go w celu odświeżenia schematu buforowanego przez bazę danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="fbf2c-105">Jeśli zostanie określona wartość "SyncMemberName", spowoduje to odświeżenie schematu bazy danych członka. Jeśli nie, zostanie odświeżony schemat bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="fbf2c-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbf2c-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf2c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fbf2c-107">DESCRIPTION</span></span>
<span data-ttu-id="fbf2c-108">Polecenie cmdlet **Update-AzSqlSyncSchema** aktualizuje schemat synchronizacji dla bazy danych członka synchronizacji lub bazy danych Centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="fbf2c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbf2c-109">EXAMPLES</span></span>

### <span data-ttu-id="fbf2c-110">Przykład 1: aktualizowanie schematu synchronizacji dla bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="fbf2c-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="fbf2c-111">To polecenie aktualizuje schemat synchronizacji dla bazy danych centrum w grupie synchronizacja syncGroup01</span><span class="sxs-lookup"><span data-stu-id="fbf2c-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="fbf2c-112">Przykład 2: aktualizowanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="fbf2c-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="fbf2c-113">To polecenie aktualizuje schemat synchronizacji bazy danych elementu członkowskiego w synchronizacji elementu członkowskiego synchronizacji syncMember01</span><span class="sxs-lookup"><span data-stu-id="fbf2c-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="fbf2c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbf2c-114">PARAMETERS</span></span>

### <span data-ttu-id="fbf2c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbf2c-115">-DatabaseName</span></span>
<span data-ttu-id="fbf2c-116">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="fbf2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf2c-117">-DefaultProfile</span></span>
<span data-ttu-id="fbf2c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fbf2c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbf2c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbf2c-119">-PassThru</span></span>
<span data-ttu-id="fbf2c-120">Określa, czy ma być zwracana Grupa synchronizacji, na której działa to polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="fbf2c-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="fbf2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbf2c-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbf2c-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fbf2c-123">-ServerName</span></span>
<span data-ttu-id="fbf2c-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fbf2c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf2c-125">-SyncGroupName</span></span>
<span data-ttu-id="fbf2c-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-126">The sync group name.</span></span>

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

### <span data-ttu-id="fbf2c-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="fbf2c-127">-SyncMemberName</span></span>
<span data-ttu-id="fbf2c-128">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf2c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbf2c-129">-Confirm</span></span>
<span data-ttu-id="fbf2c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbf2c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf2c-131">-WhatIf</span></span>
<span data-ttu-id="fbf2c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbf2c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbf2c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf2c-134">CommonParameters</span></span>
<span data-ttu-id="fbf2c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf2c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf2c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbf2c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf2c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbf2c-137">INPUTS</span></span>

### <span data-ttu-id="fbf2c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fbf2c-138">System.String</span></span>

## <span data-ttu-id="fbf2c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbf2c-139">OUTPUTS</span></span>

### <span data-ttu-id="fbf2c-140">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="fbf2c-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fbf2c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbf2c-141">NOTES</span></span>

## <span data-ttu-id="fbf2c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbf2c-142">RELATED LINKS</span></span>
