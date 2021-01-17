---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359947"
---
# <span data-ttu-id="439c7-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="439c7-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="439c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="439c7-102">SYNOPSIS</span></span>
<span data-ttu-id="439c7-103">Tworzy nowe zasady kopii zapasowej plików usługi Azure NetApp (ANF) dla konta usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="439c7-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="439c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="439c7-104">SYNTAX</span></span>

### <span data-ttu-id="439c7-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="439c7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439c7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="439c7-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439c7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="439c7-107">DESCRIPTION</span></span>
<span data-ttu-id="439c7-108">Polecenie cmdlet **New-AzNetAppFilesActiveDirectory** tworzy nowe zasady tworzenia kopii zapasowych dla konta usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="439c7-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="439c7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="439c7-109">EXAMPLES</span></span>

### <span data-ttu-id="439c7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="439c7-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="439c7-111">To polecenie tworzy nowe zasady ANF kopii zapasowej dla konta ANF o nazwie Account (Moje konto).</span><span class="sxs-lookup"><span data-stu-id="439c7-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="439c7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="439c7-112">PARAMETERS</span></span>

### <span data-ttu-id="439c7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="439c7-113">-AccountName</span></span>
<span data-ttu-id="439c7-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="439c7-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="439c7-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="439c7-115">-AccountObject</span></span>
<span data-ttu-id="439c7-116">Obiekt konta dla nowych zasad tworzenia kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="439c7-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="439c7-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="439c7-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="439c7-118">Liczba codziennych kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="439c7-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="439c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439c7-119">-DefaultProfile</span></span>
<span data-ttu-id="439c7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="439c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439c7-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="439c7-121">-Enabled</span></span>
<span data-ttu-id="439c7-122">Właściwość decydowania o zasadach jest włączona lub nie</span><span class="sxs-lookup"><span data-stu-id="439c7-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="439c7-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="439c7-123">-Location</span></span>
<span data-ttu-id="439c7-124">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="439c7-124">The location of the resource</span></span>

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

### <span data-ttu-id="439c7-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="439c7-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="439c7-126">Liczba comiesięcznych kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="439c7-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="439c7-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="439c7-127">-Name</span></span>
<span data-ttu-id="439c7-128">Nazwa zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="439c7-128">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="439c7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439c7-129">-ResourceGroupName</span></span>
<span data-ttu-id="439c7-130">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="439c7-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="439c7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="439c7-131">-Tag</span></span>
<span data-ttu-id="439c7-132">Tablica Hashtable przedstawiająca znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="439c7-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="439c7-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="439c7-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="439c7-134">Tygodniowa liczba kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="439c7-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="439c7-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="439c7-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="439c7-136">Roczna liczba kopii zapasowych do zachowania</span><span class="sxs-lookup"><span data-stu-id="439c7-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="439c7-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="439c7-137">-Confirm</span></span>
<span data-ttu-id="439c7-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439c7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="439c7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439c7-139">-WhatIf</span></span>
<span data-ttu-id="439c7-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439c7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439c7-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="439c7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="439c7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439c7-142">CommonParameters</span></span>
<span data-ttu-id="439c7-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439c7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439c7-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="439c7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439c7-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="439c7-145">INPUTS</span></span>

### <span data-ttu-id="439c7-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="439c7-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="439c7-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="439c7-147">OUTPUTS</span></span>

### <span data-ttu-id="439c7-148">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="439c7-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="439c7-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="439c7-149">NOTES</span></span>

## <span data-ttu-id="439c7-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="439c7-150">RELATED LINKS</span></span>
