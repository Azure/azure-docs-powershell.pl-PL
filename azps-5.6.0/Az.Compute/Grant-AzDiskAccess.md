---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 709fab1ab8ba39193ef9831cd03d7b1cd53208dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001770"
---
# <span data-ttu-id="a3fd2-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a3fd2-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="a3fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fd2-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="a3fd2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3fd2-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3fd2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a3fd2-106">Polecenie cmdlet **Grant-AzAccess** udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="a3fd2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3fd2-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fd2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3fd2-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="a3fd2-109">Udzielanie dostępu do dysku o nazwie "Dysk01" w grupie zasobów o nazwie "Grupa Zasobów01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="a3fd2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3fd2-110">PARAMETERS</span></span>

### <span data-ttu-id="a3fd2-111">— Access</span><span class="sxs-lookup"><span data-stu-id="a3fd2-111">-Access</span></span>
<span data-ttu-id="a3fd2-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd2-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a3fd2-113">-AsJob</span></span>
<span data-ttu-id="a3fd2-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3fd2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3fd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fd2-115">-DefaultProfile</span></span>
<span data-ttu-id="a3fd2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3fd2-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a3fd2-117">-DiskName</span></span>
<span data-ttu-id="a3fd2-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a3fd2-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="a3fd2-119">-DurationInSecond</span></span>
<span data-ttu-id="a3fd2-120">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3fd2-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a3fd2-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3fd2-123">-Confirm</span></span>
<span data-ttu-id="a3fd2-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3fd2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3fd2-125">-WhatIf</span></span>
<span data-ttu-id="a3fd2-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3fd2-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3fd2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fd2-128">CommonParameters</span></span>
<span data-ttu-id="a3fd2-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fd2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fd2-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3fd2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fd2-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3fd2-131">INPUTS</span></span>

### <span data-ttu-id="a3fd2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a3fd2-132">System.String</span></span>

## <span data-ttu-id="a3fd2-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3fd2-133">OUTPUTS</span></span>

### <span data-ttu-id="a3fd2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="a3fd2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="a3fd2-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3fd2-135">NOTES</span></span>

## <span data-ttu-id="a3fd2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3fd2-136">RELATED LINKS</span></span>
