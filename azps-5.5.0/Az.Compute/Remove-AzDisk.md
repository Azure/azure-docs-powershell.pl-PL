---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199227"
---
# <span data-ttu-id="7e6b1-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="7e6b1-101">Remove-AzDisk</span></span>

## <span data-ttu-id="7e6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6b1-103">Usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-103">Removes a disk.</span></span>

## <span data-ttu-id="7e6b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e6b1-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e6b1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e6b1-106">Polecenie **cmdlet Remove-AzCm** usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="7e6b1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e6b1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e6b1-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="7e6b1-109">To polecenie usuwa dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="7e6b1-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7e6b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="7e6b1-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7e6b1-111">-AsJob</span></span>
<span data-ttu-id="7e6b1-112">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7e6b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6b1-113">-DefaultProfile</span></span>
<span data-ttu-id="7e6b1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e6b1-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7e6b1-115">-DiskName</span></span>
<span data-ttu-id="7e6b1-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6b1-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7e6b1-117">-Force</span></span>
<span data-ttu-id="7e6b1-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e6b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e6b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e6b1-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7e6b1-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e6b1-121">-Confirm</span></span>
<span data-ttu-id="7e6b1-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e6b1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e6b1-123">-WhatIf</span></span>
<span data-ttu-id="7e6b1-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e6b1-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e6b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6b1-126">CommonParameters</span></span>
<span data-ttu-id="7e6b1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6b1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e6b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6b1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e6b1-129">INPUTS</span></span>

### <span data-ttu-id="7e6b1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7e6b1-130">System.String</span></span>

## <span data-ttu-id="7e6b1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e6b1-131">OUTPUTS</span></span>

### <span data-ttu-id="7e6b1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7e6b1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7e6b1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e6b1-133">NOTES</span></span>

## <span data-ttu-id="7e6b1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e6b1-134">RELATED LINKS</span></span>
