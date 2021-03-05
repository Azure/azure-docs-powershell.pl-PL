---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001754"
---
# <span data-ttu-id="3e853-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3e853-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="3e853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e853-102">SYNOPSIS</span></span>
<span data-ttu-id="3e853-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="3e853-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="3e853-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e853-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e853-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e853-105">DESCRIPTION</span></span>
<span data-ttu-id="3e853-106">Polecenie cmdlet **Grant-AzSnapshotAccess** udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="3e853-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="3e853-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e853-107">EXAMPLES</span></span>

### <span data-ttu-id="3e853-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e853-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="3e853-109">Udzielanie dostępu do odczytu migawki o nazwie "Migawka01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="3e853-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="3e853-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e853-110">PARAMETERS</span></span>

### <span data-ttu-id="3e853-111">— Access</span><span class="sxs-lookup"><span data-stu-id="3e853-111">-Access</span></span>
<span data-ttu-id="3e853-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="3e853-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="3e853-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3e853-113">-AsJob</span></span>
<span data-ttu-id="3e853-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3e853-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e853-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e853-115">-DefaultProfile</span></span>
<span data-ttu-id="3e853-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e853-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e853-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="3e853-117">-DurationInSecond</span></span>
<span data-ttu-id="3e853-118">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3e853-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="3e853-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e853-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e853-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e853-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3e853-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="3e853-121">-SnapshotName</span></span>
<span data-ttu-id="3e853-122">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="3e853-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="3e853-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e853-123">-Confirm</span></span>
<span data-ttu-id="3e853-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e853-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e853-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e853-125">-WhatIf</span></span>
<span data-ttu-id="3e853-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e853-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e853-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e853-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e853-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e853-128">CommonParameters</span></span>
<span data-ttu-id="3e853-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e853-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e853-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e853-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e853-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e853-131">INPUTS</span></span>

### <span data-ttu-id="3e853-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3e853-132">System.String</span></span>

## <span data-ttu-id="3e853-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e853-133">OUTPUTS</span></span>

### <span data-ttu-id="3e853-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="3e853-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="3e853-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e853-135">NOTES</span></span>

## <span data-ttu-id="3e853-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e853-136">RELATED LINKS</span></span>
