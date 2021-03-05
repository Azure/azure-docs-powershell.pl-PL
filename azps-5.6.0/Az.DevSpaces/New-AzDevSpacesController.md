---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 097248e06acd081582ecc34a863658b2b073ef60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004209"
---
# <span data-ttu-id="1202a-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1202a-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="1202a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1202a-102">SYNOPSIS</span></span>
<span data-ttu-id="1202a-103">Utwórz nowy kontroler Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1202a-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="1202a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1202a-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1202a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1202a-105">DESCRIPTION</span></span>
<span data-ttu-id="1202a-106">Utwórz nowy kontroler Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1202a-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="1202a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1202a-107">EXAMPLES</span></span>

### <span data-ttu-id="1202a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1202a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1202a-109">Utwórz kontroler DevSpaces w grupie zasobów devSpaceResourceGroup o nazwie devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="1202a-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="1202a-110">Użyj klastru clusterName jako obiektu docelowego dla tego kontrolera.</span><span class="sxs-lookup"><span data-stu-id="1202a-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="1202a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1202a-111">PARAMETERS</span></span>

### <span data-ttu-id="1202a-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1202a-112">-AsJob</span></span>
<span data-ttu-id="1202a-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1202a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1202a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1202a-114">-DefaultProfile</span></span>
<span data-ttu-id="1202a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1202a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1202a-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1202a-116">-Name</span></span>
<span data-ttu-id="1202a-117">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1202a-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1202a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1202a-118">-ResourceGroupName</span></span>
<span data-ttu-id="1202a-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1202a-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1202a-120">— Tag</span><span class="sxs-lookup"><span data-stu-id="1202a-120">-Tag</span></span>
<span data-ttu-id="1202a-121">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="1202a-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1202a-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="1202a-122">-TargetClusterName</span></span>
<span data-ttu-id="1202a-123">Target Cluster Name (Nazwa klastrów docelowych).</span><span class="sxs-lookup"><span data-stu-id="1202a-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1202a-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1202a-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="1202a-125">Nazwa grupy zasobów docelowych.</span><span class="sxs-lookup"><span data-stu-id="1202a-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="1202a-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1202a-126">-Confirm</span></span>
<span data-ttu-id="1202a-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1202a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1202a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1202a-128">-WhatIf</span></span>
<span data-ttu-id="1202a-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1202a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1202a-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1202a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1202a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1202a-131">CommonParameters</span></span>
<span data-ttu-id="1202a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1202a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1202a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1202a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1202a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1202a-134">INPUTS</span></span>

### <span data-ttu-id="1202a-135">Brak</span><span class="sxs-lookup"><span data-stu-id="1202a-135">None</span></span>

## <span data-ttu-id="1202a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1202a-136">OUTPUTS</span></span>

### <span data-ttu-id="1202a-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="1202a-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1202a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1202a-138">NOTES</span></span>

## <span data-ttu-id="1202a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1202a-139">RELATED LINKS</span></span>
