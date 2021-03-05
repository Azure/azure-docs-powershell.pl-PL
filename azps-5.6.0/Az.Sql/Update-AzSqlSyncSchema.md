---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 394ae4d82437795f62e19b4d0f7a536cdd893da9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992244"
---
# <span data-ttu-id="4cc9b-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="4cc9b-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="4cc9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc9b-103">Zaktualizuj schemat synchronizacji dla bazy danych członka synchronizacji lub bazy danych centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="4cc9b-104">Pobierze on najnowszy schemat bazy danych z rzeczywistej bazy danych, a następnie użyje go do odświeżenia schematu buforowanej przez synchronizowanie baza metadanych.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="4cc9b-105">Jeśli zostanie określona nazwa "SyncMemberName", odświeży ona schemat bazy danych członków. Jeśli nie, odświeży schemat bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="4cc9b-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cc9b-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc9b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cc9b-107">DESCRIPTION</span></span>
<span data-ttu-id="4cc9b-108">Polecenie **cmdlet Update-AzSqlSyncSchema** aktualizuje schemat synchronizacji bazy danych członka synchronizacji lub bazy danych centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="4cc9b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cc9b-109">EXAMPLES</span></span>

### <span data-ttu-id="4cc9b-110">Przykład 1. Aktualizowanie schematu synchronizacji bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="4cc9b-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="4cc9b-111">To polecenie aktualizuje schemat synchronizacji bazy danych centrum w grupie synchronizacji SyncGroup01</span><span class="sxs-lookup"><span data-stu-id="4cc9b-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="4cc9b-112">Przykład 2. Aktualizowanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="4cc9b-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="4cc9b-113">To polecenie aktualizuje schemat synchronizacji dla bazy danych członków w pliku syncMember01 członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="4cc9b-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="4cc9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cc9b-114">PARAMETERS</span></span>

### <span data-ttu-id="4cc9b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4cc9b-115">-DatabaseName</span></span>
<span data-ttu-id="4cc9b-116">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4cc9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc9b-117">-DefaultProfile</span></span>
<span data-ttu-id="4cc9b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4cc9b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cc9b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cc9b-119">-PassThru</span></span>
<span data-ttu-id="4cc9b-120">Definiuje, czy zwracana jest grupa synchronizacji, na podstawie których działa to polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cc9b-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="4cc9b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc9b-121">-ResourceGroupName</span></span>
<span data-ttu-id="4cc9b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cc9b-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4cc9b-123">-ServerName</span></span>
<span data-ttu-id="4cc9b-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4cc9b-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc9b-125">-SyncGroupName</span></span>
<span data-ttu-id="4cc9b-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-126">The sync group name.</span></span>

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

### <span data-ttu-id="4cc9b-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="4cc9b-127">-SyncMemberName</span></span>
<span data-ttu-id="4cc9b-128">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-128">The sync member name.</span></span>

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

### <span data-ttu-id="4cc9b-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cc9b-129">-Confirm</span></span>
<span data-ttu-id="4cc9b-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc9b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc9b-131">-WhatIf</span></span>
<span data-ttu-id="4cc9b-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc9b-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc9b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc9b-134">CommonParameters</span></span>
<span data-ttu-id="4cc9b-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc9b-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cc9b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc9b-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc9b-137">INPUTS</span></span>

### <span data-ttu-id="4cc9b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4cc9b-138">System.String</span></span>

## <span data-ttu-id="4cc9b-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc9b-139">OUTPUTS</span></span>

### <span data-ttu-id="4cc9b-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4cc9b-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4cc9b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cc9b-141">NOTES</span></span>

## <span data-ttu-id="4cc9b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cc9b-142">RELATED LINKS</span></span>
