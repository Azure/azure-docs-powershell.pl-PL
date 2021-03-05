---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988366"
---
# <span data-ttu-id="e67e1-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e67e1-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="e67e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e67e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e67e1-103">Usuwa zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e67e1-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="e67e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e67e1-104">SYNTAX</span></span>

### <span data-ttu-id="e67e1-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e67e1-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67e1-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="e67e1-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67e1-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="e67e1-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e67e1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e67e1-108">DESCRIPTION</span></span>
<span data-ttu-id="e67e1-109">Usuwa zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e67e1-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="e67e1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e67e1-110">EXAMPLES</span></span>

### <span data-ttu-id="e67e1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e67e1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="e67e1-112">Usuwanie zestawu szyfrowania dysku "enc1" w "rg1"</span><span class="sxs-lookup"><span data-stu-id="e67e1-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="e67e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e67e1-113">PARAMETERS</span></span>

### <span data-ttu-id="e67e1-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e67e1-114">-AsJob</span></span>
<span data-ttu-id="e67e1-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e67e1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e67e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67e1-116">-DefaultProfile</span></span>
<span data-ttu-id="e67e1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e67e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e67e1-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e67e1-118">-Force</span></span>
<span data-ttu-id="e67e1-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e67e1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e67e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e67e1-120">-InputObject</span></span>
<span data-ttu-id="e67e1-121">Obiekt lokalny zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e67e1-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e67e1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e67e1-122">-Name</span></span>
<span data-ttu-id="e67e1-123">Nazwa zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e67e1-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e67e1-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e67e1-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e67e1-126">-ResourceId</span></span>
<span data-ttu-id="e67e1-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67e1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e67e1-128">-Confirm</span></span>
<span data-ttu-id="e67e1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e67e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e67e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67e1-130">-WhatIf</span></span>
<span data-ttu-id="e67e1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e67e1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e67e1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e67e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e67e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67e1-133">CommonParameters</span></span>
<span data-ttu-id="e67e1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67e1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e67e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67e1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e67e1-136">INPUTS</span></span>

### <span data-ttu-id="e67e1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e67e1-137">System.String</span></span>

### <span data-ttu-id="e67e1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e67e1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e67e1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e67e1-139">OUTPUTS</span></span>

### <span data-ttu-id="e67e1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e67e1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e67e1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e67e1-141">NOTES</span></span>

## <span data-ttu-id="e67e1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e67e1-142">RELATED LINKS</span></span>
