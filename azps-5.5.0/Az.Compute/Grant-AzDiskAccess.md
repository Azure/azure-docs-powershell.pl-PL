---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244130"
---
# <span data-ttu-id="2429c-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2429c-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="2429c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2429c-102">SYNOPSIS</span></span>
<span data-ttu-id="2429c-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2429c-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="2429c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2429c-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2429c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2429c-105">DESCRIPTION</span></span>
<span data-ttu-id="2429c-106">Polecenie cmdlet **Grant-AzAccess** udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2429c-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="2429c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2429c-107">EXAMPLES</span></span>

### <span data-ttu-id="2429c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2429c-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="2429c-109">Ułagodz "Odczyt" dostęp do dysku o nazwie "Dysk01" w grupie zasobów o nazwie "Grupa Zasobów01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="2429c-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="2429c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2429c-110">PARAMETERS</span></span>

### <span data-ttu-id="2429c-111">— Access</span><span class="sxs-lookup"><span data-stu-id="2429c-111">-Access</span></span>
<span data-ttu-id="2429c-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="2429c-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="2429c-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2429c-113">-AsJob</span></span>
<span data-ttu-id="2429c-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2429c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2429c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2429c-115">-DefaultProfile</span></span>
<span data-ttu-id="2429c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2429c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2429c-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2429c-117">-DiskName</span></span>
<span data-ttu-id="2429c-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="2429c-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2429c-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="2429c-119">-DurationInSecond</span></span>
<span data-ttu-id="2429c-120">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="2429c-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="2429c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2429c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2429c-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2429c-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2429c-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2429c-123">-Confirm</span></span>
<span data-ttu-id="2429c-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2429c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2429c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2429c-125">-WhatIf</span></span>
<span data-ttu-id="2429c-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2429c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2429c-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2429c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2429c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2429c-128">CommonParameters</span></span>
<span data-ttu-id="2429c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2429c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2429c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2429c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2429c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2429c-131">INPUTS</span></span>

### <span data-ttu-id="2429c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2429c-132">System.String</span></span>

## <span data-ttu-id="2429c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2429c-133">OUTPUTS</span></span>

### <span data-ttu-id="2429c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="2429c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="2429c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2429c-135">NOTES</span></span>

## <span data-ttu-id="2429c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2429c-136">RELATED LINKS</span></span>
