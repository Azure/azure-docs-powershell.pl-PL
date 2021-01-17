---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335293"
---
# <span data-ttu-id="a1b59-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b59-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a1b59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1b59-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b59-103">Umożliwia zaktualizowanie zasad tworzenia kopii zapasowych plików usługi Azure NetApp (ANF) do dodanych opcjonalnych modyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="a1b59-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="a1b59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1b59-104">SYNTAX</span></span>

### <span data-ttu-id="a1b59-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1b59-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b59-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b59-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b59-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b59-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b59-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b59-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b59-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a1b59-109">DESCRIPTION</span></span>
<span data-ttu-id="a1b59-110">Polecenie cmdlet **Update-AzNetAppFilesBackupPolicy** modyfikuje zasady tworzenia kopii zapasowych ANF.</span><span class="sxs-lookup"><span data-stu-id="a1b59-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="a1b59-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1b59-111">EXAMPLES</span></span>

### <span data-ttu-id="a1b59-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1b59-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="a1b59-113">To polecenie powoduje zmianę zasad tworzenia kopii zapasowej ANF "MyBackupPolicy", aby uzyskać dane DailyBackupsToKeep.</span><span class="sxs-lookup"><span data-stu-id="a1b59-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="a1b59-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1b59-114">PARAMETERS</span></span>

### <span data-ttu-id="a1b59-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a1b59-115">-AccountName</span></span>
<span data-ttu-id="a1b59-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="a1b59-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a1b59-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="a1b59-117">-AccountObject</span></span>
<span data-ttu-id="a1b59-118">Obiekt konta zawierający zasady tworzenia kopii zapasowych do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a1b59-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="a1b59-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="a1b59-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="a1b59-120">Liczba codziennych kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="a1b59-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="a1b59-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b59-121">-DefaultProfile</span></span>
<span data-ttu-id="a1b59-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b59-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b59-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1b59-123">-InputObject</span></span>
<span data-ttu-id="a1b59-124">Obiekt BackupPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a1b59-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b59-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a1b59-125">-Location</span></span>
<span data-ttu-id="a1b59-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a1b59-126">The location of the resource</span></span>

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

### <span data-ttu-id="a1b59-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="a1b59-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="a1b59-128">Liczba comiesięcznych kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="a1b59-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="a1b59-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1b59-129">-Name</span></span>
<span data-ttu-id="a1b59-130">Nazwa zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="a1b59-130">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b59-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b59-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1b59-132">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="a1b59-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a1b59-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b59-133">-ResourceId</span></span>
<span data-ttu-id="a1b59-134">Identyfikator zasobu zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="a1b59-134">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b59-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1b59-135">-Tag</span></span>
<span data-ttu-id="a1b59-136">Tablica Hashtable przedstawiająca znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="a1b59-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="a1b59-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="a1b59-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="a1b59-138">Tygodniowa liczba kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="a1b59-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="a1b59-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="a1b59-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="a1b59-140">Roczna liczba kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="a1b59-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="a1b59-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1b59-141">-Confirm</span></span>
<span data-ttu-id="a1b59-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b59-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b59-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b59-143">-WhatIf</span></span>
<span data-ttu-id="a1b59-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b59-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b59-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1b59-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b59-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b59-146">CommonParameters</span></span>
<span data-ttu-id="a1b59-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b59-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b59-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1b59-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b59-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1b59-149">INPUTS</span></span>

### <span data-ttu-id="a1b59-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b59-150">System.String</span></span>

### <span data-ttu-id="a1b59-151">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a1b59-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a1b59-152">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b59-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a1b59-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1b59-153">OUTPUTS</span></span>

### <span data-ttu-id="a1b59-154">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a1b59-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a1b59-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1b59-155">NOTES</span></span>

## <span data-ttu-id="a1b59-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1b59-156">RELATED LINKS</span></span>
