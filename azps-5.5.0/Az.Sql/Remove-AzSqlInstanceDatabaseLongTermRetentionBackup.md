---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188026"
---
# <span data-ttu-id="b35c2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b35c2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="b35c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b35c2-103">Usuwa długookresową kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b35c2-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="b35c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b35c2-104">SYNTAX</span></span>

### <span data-ttu-id="b35c2-105">RemoveBackupDefault (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b35c2-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35c2-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="b35c2-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35c2-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="b35c2-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35c2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b35c2-108">DESCRIPTION</span></span>
<span data-ttu-id="b35c2-109">Polecenie **cmdlet Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** usuwa określoną kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="b35c2-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="b35c2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b35c2-110">EXAMPLES</span></span>

### <span data-ttu-id="b35c2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b35c2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="b35c2-112">Usuwa kopię zapasową o nazwie 15be823c-7e2c-49d8-819f-a3fdcad92215;13226825055000000</span><span class="sxs-lookup"><span data-stu-id="b35c2-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="b35c2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b35c2-113">PARAMETERS</span></span>

### <span data-ttu-id="b35c2-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b35c2-114">-BackupName</span></span>
<span data-ttu-id="b35c2-115">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b35c2-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b35c2-116">-DatabaseName</span></span>
<span data-ttu-id="b35c2-117">Nazwa zarządzanej bazy danych, z których pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="b35c2-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35c2-118">-DefaultProfile</span></span>
<span data-ttu-id="b35c2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b35c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35c2-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b35c2-120">-Force</span></span>
<span data-ttu-id="b35c2-121">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="b35c2-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b35c2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b35c2-122">-InputObject</span></span>
<span data-ttu-id="b35c2-123">Obiekt długookresowej kopii zapasowej przechowywania bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b35c2-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b35c2-124">-InstanceName</span></span>
<span data-ttu-id="b35c2-125">Nazwa zarządzanego wystąpienia kopii zapasowej znajduje się poniżej.</span><span class="sxs-lookup"><span data-stu-id="b35c2-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b35c2-126">-Location</span></span>
<span data-ttu-id="b35c2-127">Lokalizacja źródłowego wystąpienia zarządzanego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b35c2-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="b35c2-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b35c2-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b35c2-130">-ResourceId</span></span>
<span data-ttu-id="b35c2-131">Identyfikator zasobu kopii zapasowej przechowywania długoterminowego bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b35c2-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35c2-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b35c2-132">-Confirm</span></span>
<span data-ttu-id="b35c2-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b35c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35c2-134">-WhatIf</span></span>
<span data-ttu-id="b35c2-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b35c2-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b35c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35c2-137">CommonParameters</span></span>
<span data-ttu-id="b35c2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35c2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b35c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35c2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35c2-140">INPUTS</span></span>

### <span data-ttu-id="b35c2-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="b35c2-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="b35c2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b35c2-142">System.String</span></span>

## <span data-ttu-id="b35c2-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b35c2-143">OUTPUTS</span></span>

### <span data-ttu-id="b35c2-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="b35c2-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="b35c2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b35c2-145">NOTES</span></span>

## <span data-ttu-id="b35c2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b35c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="b35c2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b35c2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b35c2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b35c2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b35c2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b35c2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b35c2-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b35c2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)