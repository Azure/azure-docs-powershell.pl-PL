---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 767104edb73265f472e155e8d003b0b5e96906e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963226"
---
# <span data-ttu-id="1a64c-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1a64c-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="1a64c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a64c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a64c-103">Cofa dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="1a64c-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="1a64c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a64c-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a64c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a64c-105">DESCRIPTION</span></span>
<span data-ttu-id="1a64c-106">Polecenie cmdlet **Revoke-AzAccess** odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="1a64c-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="1a64c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a64c-107">EXAMPLES</span></span>

### <span data-ttu-id="1a64c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a64c-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="1a64c-109">Odwoływanie dostępu do dysku o nazwie "Dysk01" w grupie zasobów o nazwie "Grupa Zasobów01"</span><span class="sxs-lookup"><span data-stu-id="1a64c-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="1a64c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a64c-110">PARAMETERS</span></span>

### <span data-ttu-id="1a64c-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1a64c-111">-AsJob</span></span>
<span data-ttu-id="1a64c-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a64c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a64c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a64c-113">-DefaultProfile</span></span>
<span data-ttu-id="1a64c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a64c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a64c-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1a64c-115">-DiskName</span></span>
<span data-ttu-id="1a64c-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="1a64c-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="1a64c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a64c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a64c-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a64c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1a64c-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a64c-119">-Confirm</span></span>
<span data-ttu-id="1a64c-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a64c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a64c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a64c-121">-WhatIf</span></span>
<span data-ttu-id="1a64c-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a64c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a64c-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a64c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a64c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a64c-124">CommonParameters</span></span>
<span data-ttu-id="1a64c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a64c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a64c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a64c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a64c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a64c-127">INPUTS</span></span>

### <span data-ttu-id="1a64c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1a64c-128">System.String</span></span>

## <span data-ttu-id="1a64c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a64c-129">OUTPUTS</span></span>

### <span data-ttu-id="1a64c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1a64c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1a64c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a64c-131">NOTES</span></span>

## <span data-ttu-id="1a64c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a64c-132">RELATED LINKS</span></span>
