---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969217"
---
# <span data-ttu-id="8a279-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="8a279-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="8a279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a279-102">SYNOPSIS</span></span>
<span data-ttu-id="8a279-103">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="8a279-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="8a279-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a279-104">SYNTAX</span></span>

### <span data-ttu-id="8a279-105">DevSpacesControllerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8a279-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a279-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a279-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a279-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a279-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a279-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a279-108">DESCRIPTION</span></span>
<span data-ttu-id="8a279-109">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="8a279-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="8a279-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a279-110">EXAMPLES</span></span>

### <span data-ttu-id="8a279-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a279-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="8a279-112">Usuń kontroler DevSpaces o nazwie devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="8a279-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="8a279-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a279-113">PARAMETERS</span></span>

### <span data-ttu-id="8a279-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8a279-114">-AsJob</span></span>
<span data-ttu-id="8a279-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a279-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a279-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a279-116">-DefaultProfile</span></span>
<span data-ttu-id="8a279-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a279-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a279-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a279-118">-InputObject</span></span>
<span data-ttu-id="8a279-119">Obiekt PSController, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="8a279-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a279-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a279-120">-Name</span></span>
<span data-ttu-id="8a279-121">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="8a279-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a279-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a279-122">-PassThru</span></span>
<span data-ttu-id="8a279-123">Zwraca wartość prawda, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="8a279-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="8a279-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a279-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a279-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8a279-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a279-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a279-126">-ResourceId</span></span>
<span data-ttu-id="8a279-127">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="8a279-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a279-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a279-128">-Confirm</span></span>
<span data-ttu-id="8a279-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a279-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a279-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a279-130">-WhatIf</span></span>
<span data-ttu-id="8a279-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a279-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a279-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8a279-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a279-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a279-133">CommonParameters</span></span>
<span data-ttu-id="8a279-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a279-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a279-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a279-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a279-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a279-136">INPUTS</span></span>

### <span data-ttu-id="8a279-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8a279-137">System.String</span></span>

### <span data-ttu-id="8a279-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="8a279-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="8a279-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a279-139">OUTPUTS</span></span>

### <span data-ttu-id="8a279-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a279-140">System.Boolean</span></span>

## <span data-ttu-id="8a279-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a279-141">NOTES</span></span>

## <span data-ttu-id="8a279-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a279-142">RELATED LINKS</span></span>
