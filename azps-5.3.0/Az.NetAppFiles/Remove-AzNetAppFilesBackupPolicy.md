---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499638"
---
# <span data-ttu-id="5a791-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5a791-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5a791-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a791-102">SYNOPSIS</span></span>
<span data-ttu-id="5a791-103">Usuwa zasady kopii zapasowej plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5a791-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="5a791-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a791-104">SYNTAX</span></span>

### <span data-ttu-id="5a791-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a791-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a791-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a791-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a791-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a791-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a791-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a791-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a791-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5a791-109">DESCRIPTION</span></span>
<span data-ttu-id="5a791-110">Polecenie cmdlet **Remove-AzNetAppFilesBackupPolicy** usuwa ANFą zasadę tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="5a791-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="5a791-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a791-111">EXAMPLES</span></span>

### <span data-ttu-id="5a791-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a791-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="5a791-113">To polecenie usuwa nowe zasady ANF kopii zapasowej z nazwą "MyBackupPolicy" dla konta "Moje konto".</span><span class="sxs-lookup"><span data-stu-id="5a791-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="5a791-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a791-114">PARAMETERS</span></span>

### <span data-ttu-id="5a791-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a791-115">-AccountName</span></span>
<span data-ttu-id="5a791-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="5a791-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="5a791-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="5a791-117">-AccountObject</span></span>
<span data-ttu-id="5a791-118">Obiekt konta zawierający zasady tworzenia kopii zapasowych do usunięcia</span><span class="sxs-lookup"><span data-stu-id="5a791-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="5a791-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a791-119">-DefaultProfile</span></span>
<span data-ttu-id="5a791-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a791-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a791-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a791-121">-InputObject</span></span>
<span data-ttu-id="5a791-122">Obiekt BackupPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="5a791-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="5a791-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a791-123">-Name</span></span>
<span data-ttu-id="5a791-124">Nazwa zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="5a791-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="5a791-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a791-125">-PassThru</span></span>
<span data-ttu-id="5a791-126">Zwraca, czy określone zasady tworzenia kopii zapasowych zostały pomyślnie usunięte</span><span class="sxs-lookup"><span data-stu-id="5a791-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="5a791-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a791-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a791-128">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="5a791-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5a791-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a791-129">-ResourceId</span></span>
<span data-ttu-id="5a791-130">Identyfikator zasobu zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="5a791-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="5a791-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a791-131">-Confirm</span></span>
<span data-ttu-id="5a791-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a791-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a791-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a791-133">-WhatIf</span></span>
<span data-ttu-id="5a791-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a791-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a791-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a791-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a791-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a791-136">CommonParameters</span></span>
<span data-ttu-id="5a791-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a791-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a791-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a791-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a791-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a791-139">INPUTS</span></span>

### <span data-ttu-id="5a791-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5a791-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="5a791-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5a791-141">System.String</span></span>

### <span data-ttu-id="5a791-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5a791-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5a791-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a791-143">OUTPUTS</span></span>

### <span data-ttu-id="5a791-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5a791-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5a791-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a791-145">NOTES</span></span>

## <span data-ttu-id="5a791-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a791-146">RELATED LINKS</span></span>
