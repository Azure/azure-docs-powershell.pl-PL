---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203302"
---
# <span data-ttu-id="a5b39-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a5b39-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a5b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b39-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b39-103">Usuwa zasady kopii zapasowej azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="a5b39-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="a5b39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5b39-104">SYNTAX</span></span>

### <span data-ttu-id="a5b39-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a5b39-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b39-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b39-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b39-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b39-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b39-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b39-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b39-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5b39-109">DESCRIPTION</span></span>
<span data-ttu-id="a5b39-110">Polecenie **cmdlet Remove-AzNetAppFilesBackupPolicy** usuwa zasady kopii zapasowej ANF.</span><span class="sxs-lookup"><span data-stu-id="a5b39-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="a5b39-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5b39-111">EXAMPLES</span></span>

### <span data-ttu-id="a5b39-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5b39-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="a5b39-113">To polecenie usuwa nowe zasady kopii zapasowej ANF o nazwie "MyBackupPolicy" dla konta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="a5b39-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="a5b39-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5b39-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b39-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5b39-115">-AccountName</span></span>
<span data-ttu-id="a5b39-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="a5b39-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a5b39-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a5b39-117">-AccountObject</span></span>
<span data-ttu-id="a5b39-118">Obiekt Account zawierający zasady kopii zapasowej do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a5b39-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="a5b39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b39-119">-DefaultProfile</span></span>
<span data-ttu-id="a5b39-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b39-121">-InputObject</span></span>
<span data-ttu-id="a5b39-122">Obiekt BackupPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a5b39-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="a5b39-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a5b39-123">-Name</span></span>
<span data-ttu-id="a5b39-124">Nazwa zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="a5b39-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="a5b39-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b39-125">-PassThru</span></span>
<span data-ttu-id="a5b39-126">Zwracanie, czy określone zasady kopii zapasowej zostały pomyślnie usunięte</span><span class="sxs-lookup"><span data-stu-id="a5b39-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="a5b39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b39-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5b39-128">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="a5b39-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a5b39-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b39-129">-ResourceId</span></span>
<span data-ttu-id="a5b39-130">Identyfikator zasobu zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="a5b39-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="a5b39-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5b39-131">-Confirm</span></span>
<span data-ttu-id="a5b39-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5b39-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b39-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b39-133">-WhatIf</span></span>
<span data-ttu-id="a5b39-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b39-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b39-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a5b39-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b39-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b39-136">CommonParameters</span></span>
<span data-ttu-id="a5b39-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b39-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b39-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b39-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b39-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5b39-139">INPUTS</span></span>

### <span data-ttu-id="a5b39-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5b39-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a5b39-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a5b39-141">System.String</span></span>

### <span data-ttu-id="a5b39-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a5b39-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a5b39-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5b39-143">OUTPUTS</span></span>

### <span data-ttu-id="a5b39-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a5b39-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a5b39-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5b39-145">NOTES</span></span>

## <span data-ttu-id="a5b39-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5b39-146">RELATED LINKS</span></span>
