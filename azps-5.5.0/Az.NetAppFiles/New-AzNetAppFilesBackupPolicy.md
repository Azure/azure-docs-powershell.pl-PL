---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203315"
---
# <span data-ttu-id="52fff-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="52fff-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="52fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52fff-102">SYNOPSIS</span></span>
<span data-ttu-id="52fff-103">Tworzy nowe zasady kopii zapasowej plików ANF (Azure NetApp Files) dla konta ANF.</span><span class="sxs-lookup"><span data-stu-id="52fff-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="52fff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52fff-104">SYNTAX</span></span>

### <span data-ttu-id="52fff-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="52fff-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52fff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52fff-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fff-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="52fff-107">DESCRIPTION</span></span>
<span data-ttu-id="52fff-108">Polecenie **cmdlet New-AzNetAppFilesActiveDirectory** tworzy nowe zasady kopii zapasowej dla konta ANF.</span><span class="sxs-lookup"><span data-stu-id="52fff-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="52fff-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52fff-109">EXAMPLES</span></span>

### <span data-ttu-id="52fff-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52fff-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="52fff-111">To polecenie tworzy nowe zasady kopii zapasowej ANF dla konta ANF o nazwie "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="52fff-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="52fff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52fff-112">PARAMETERS</span></span>

### <span data-ttu-id="52fff-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52fff-113">-AccountName</span></span>
<span data-ttu-id="52fff-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="52fff-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="52fff-115">-AccountObject</span></span>
<span data-ttu-id="52fff-116">Obiekt Account dla nowych zasad kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="52fff-116">The Account object for the new Backup Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="52fff-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="52fff-118">Dzienna liczba kopii zapasowych do utrzymania</span><span class="sxs-lookup"><span data-stu-id="52fff-118">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fff-119">-DefaultProfile</span></span>
<span data-ttu-id="52fff-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52fff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52fff-121">— włączone</span><span class="sxs-lookup"><span data-stu-id="52fff-121">-Enabled</span></span>
<span data-ttu-id="52fff-122">Właściwość do decydowania o włączeniu zasad jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="52fff-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="52fff-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52fff-123">-Location</span></span>
<span data-ttu-id="52fff-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="52fff-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="52fff-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="52fff-126">Miesięczne kopie zapasowe są liczone do utrzymania</span><span class="sxs-lookup"><span data-stu-id="52fff-126">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="52fff-127">-Name</span></span>
<span data-ttu-id="52fff-128">Nazwa zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="52fff-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fff-129">-ResourceGroupName</span></span>
<span data-ttu-id="52fff-130">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="52fff-130">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="52fff-131">-Tag</span></span>
<span data-ttu-id="52fff-132">Tablica z hasztagami reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="52fff-132">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="52fff-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="52fff-134">Cotygodniowe kopie zapasowe są liczone do utrzymania</span><span class="sxs-lookup"><span data-stu-id="52fff-134">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="52fff-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="52fff-136">Liczba kopii zapasowych do przechowywania</span><span class="sxs-lookup"><span data-stu-id="52fff-136">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fff-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52fff-137">-Confirm</span></span>
<span data-ttu-id="52fff-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52fff-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fff-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fff-139">-WhatIf</span></span>
<span data-ttu-id="52fff-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fff-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52fff-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52fff-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fff-142">CommonParameters</span></span>
<span data-ttu-id="52fff-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fff-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52fff-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fff-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52fff-145">INPUTS</span></span>

### <span data-ttu-id="52fff-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="52fff-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="52fff-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52fff-147">OUTPUTS</span></span>

### <span data-ttu-id="52fff-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="52fff-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="52fff-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52fff-149">NOTES</span></span>

## <span data-ttu-id="52fff-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52fff-150">RELATED LINKS</span></span>
