---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 86eb9f1389f0474fcc109b219e9eae1bd385b7b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991474"
---
# <span data-ttu-id="14201-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="14201-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="14201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14201-102">SYNOPSIS</span></span>
<span data-ttu-id="14201-103">Usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="14201-103">Removes a snapshot.</span></span>

## <span data-ttu-id="14201-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14201-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14201-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14201-105">DESCRIPTION</span></span>
<span data-ttu-id="14201-106">Polecenie **cmdlet Remove-AzSnapshot** usuwa migawkę.</span><span class="sxs-lookup"><span data-stu-id="14201-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="14201-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14201-107">EXAMPLES</span></span>

### <span data-ttu-id="14201-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14201-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="14201-109">To polecenie usuwa migawkę o nazwie "Migawka01" z grupy zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="14201-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="14201-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14201-110">PARAMETERS</span></span>

### <span data-ttu-id="14201-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="14201-111">-AsJob</span></span>
<span data-ttu-id="14201-112">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="14201-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="14201-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14201-113">-DefaultProfile</span></span>
<span data-ttu-id="14201-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14201-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14201-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="14201-115">-Force</span></span>
<span data-ttu-id="14201-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="14201-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14201-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14201-117">-ResourceGroupName</span></span>
<span data-ttu-id="14201-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14201-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="14201-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="14201-119">-SnapshotName</span></span>
<span data-ttu-id="14201-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="14201-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="14201-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14201-121">-Confirm</span></span>
<span data-ttu-id="14201-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14201-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14201-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14201-123">-WhatIf</span></span>
<span data-ttu-id="14201-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14201-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14201-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14201-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14201-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14201-126">CommonParameters</span></span>
<span data-ttu-id="14201-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14201-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14201-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14201-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14201-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14201-129">INPUTS</span></span>

### <span data-ttu-id="14201-130">System.String</span><span class="sxs-lookup"><span data-stu-id="14201-130">System.String</span></span>

## <span data-ttu-id="14201-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14201-131">OUTPUTS</span></span>

### <span data-ttu-id="14201-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="14201-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="14201-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14201-133">NOTES</span></span>

## <span data-ttu-id="14201-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14201-134">RELATED LINKS</span></span>
