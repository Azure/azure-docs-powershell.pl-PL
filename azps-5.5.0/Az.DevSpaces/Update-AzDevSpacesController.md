---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238000"
---
# <span data-ttu-id="6c15c-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6c15c-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="6c15c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c15c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c15c-103">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="6c15c-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="6c15c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c15c-104">SYNTAX</span></span>

### <span data-ttu-id="6c15c-105">DevSpacesControllerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c15c-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c15c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c15c-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c15c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c15c-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c15c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c15c-108">DESCRIPTION</span></span>
<span data-ttu-id="6c15c-109">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="6c15c-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="6c15c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c15c-110">EXAMPLES</span></span>

### <span data-ttu-id="6c15c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c15c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="6c15c-112">Otaguj kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6c15c-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="6c15c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c15c-113">PARAMETERS</span></span>

### <span data-ttu-id="6c15c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c15c-114">-DefaultProfile</span></span>
<span data-ttu-id="6c15c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c15c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c15c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c15c-116">-InputObject</span></span>
<span data-ttu-id="6c15c-117">Obiekt PSController, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="6c15c-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6c15c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c15c-118">-Name</span></span>
<span data-ttu-id="6c15c-119">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6c15c-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6c15c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c15c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c15c-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c15c-121">Resource group name</span></span>

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

### <span data-ttu-id="6c15c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c15c-122">-ResourceId</span></span>
<span data-ttu-id="6c15c-123">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="6c15c-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="6c15c-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="6c15c-124">-Tag</span></span>
<span data-ttu-id="6c15c-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c15c-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6c15c-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c15c-126">-Confirm</span></span>
<span data-ttu-id="6c15c-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c15c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c15c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c15c-128">-WhatIf</span></span>
<span data-ttu-id="6c15c-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c15c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c15c-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6c15c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c15c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c15c-131">CommonParameters</span></span>
<span data-ttu-id="6c15c-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c15c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c15c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c15c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c15c-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c15c-134">INPUTS</span></span>

### <span data-ttu-id="6c15c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6c15c-135">System.String</span></span>

### <span data-ttu-id="6c15c-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="6c15c-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6c15c-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c15c-137">OUTPUTS</span></span>

### <span data-ttu-id="6c15c-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="6c15c-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6c15c-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c15c-139">NOTES</span></span>

## <span data-ttu-id="6c15c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c15c-140">RELATED LINKS</span></span>
