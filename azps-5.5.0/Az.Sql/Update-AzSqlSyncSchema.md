---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187938"
---
# <span data-ttu-id="35e82-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="35e82-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="35e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e82-102">SYNOPSIS</span></span>
<span data-ttu-id="35e82-103">Zaktualizuj schemat synchronizacji dla bazy danych członka synchronizacji lub bazy danych centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35e82-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="35e82-104">Pobierze on najnowszy schemat bazy danych z rzeczywistej bazy danych, a następnie użyje go do odświeżenia schematu z pamięci podręcznej przez usługę baza metadanych.</span><span class="sxs-lookup"><span data-stu-id="35e82-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="35e82-105">Jeśli zostanie określona nazwa "SyncMemberName", odświeży ona schemat bazy danych członków. Jeśli nie, odświeży schemat bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="35e82-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="35e82-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35e82-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e82-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="35e82-107">DESCRIPTION</span></span>
<span data-ttu-id="35e82-108">Polecenie **cmdlet Update-AzSqlSyncSchema** aktualizuje schemat synchronizacji dla bazy danych członka synchronizacji lub bazy danych centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35e82-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="35e82-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35e82-109">EXAMPLES</span></span>

### <span data-ttu-id="35e82-110">Przykład 1. Aktualizowanie schematu synchronizacji bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="35e82-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="35e82-111">To polecenie aktualizuje schemat synchronizacji bazy danych centrum w grupie synchronizacji SyncGroup01</span><span class="sxs-lookup"><span data-stu-id="35e82-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="35e82-112">Przykład 2. Aktualizowanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="35e82-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="35e82-113">To polecenie aktualizuje schemat synchronizacji dla bazy danych członków w pliku syncMember01 członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="35e82-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="35e82-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35e82-114">PARAMETERS</span></span>

### <span data-ttu-id="35e82-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35e82-115">-DatabaseName</span></span>
<span data-ttu-id="35e82-116">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="35e82-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="35e82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e82-117">-DefaultProfile</span></span>
<span data-ttu-id="35e82-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="35e82-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35e82-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35e82-119">-PassThru</span></span>
<span data-ttu-id="35e82-120">Definiuje, czy zwracana jest grupa synchronizacji, na podstawie których działa to polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="35e82-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="35e82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e82-121">-ResourceGroupName</span></span>
<span data-ttu-id="35e82-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35e82-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="35e82-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35e82-123">-ServerName</span></span>
<span data-ttu-id="35e82-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35e82-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="35e82-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="35e82-125">-SyncGroupName</span></span>
<span data-ttu-id="35e82-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35e82-126">The sync group name.</span></span>

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

### <span data-ttu-id="35e82-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="35e82-127">-SyncMemberName</span></span>
<span data-ttu-id="35e82-128">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35e82-128">The sync member name.</span></span>

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

### <span data-ttu-id="35e82-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35e82-129">-Confirm</span></span>
<span data-ttu-id="35e82-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35e82-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e82-131">-WhatIf</span></span>
<span data-ttu-id="35e82-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e82-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e82-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="35e82-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e82-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e82-134">CommonParameters</span></span>
<span data-ttu-id="35e82-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e82-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e82-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35e82-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e82-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35e82-137">INPUTS</span></span>

### <span data-ttu-id="35e82-138">System.String</span><span class="sxs-lookup"><span data-stu-id="35e82-138">System.String</span></span>

## <span data-ttu-id="35e82-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35e82-139">OUTPUTS</span></span>

### <span data-ttu-id="35e82-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="35e82-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="35e82-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35e82-141">NOTES</span></span>

## <span data-ttu-id="35e82-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35e82-142">RELATED LINKS</span></span>
