---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012186"
---
# <span data-ttu-id="724fb-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="724fb-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="724fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724fb-102">SYNOPSIS</span></span>
<span data-ttu-id="724fb-103">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="724fb-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="724fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="724fb-104">SYNTAX</span></span>

### <span data-ttu-id="724fb-105">DevSpacesControllerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="724fb-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="724fb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="724fb-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="724fb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="724fb-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="724fb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="724fb-108">DESCRIPTION</span></span>
<span data-ttu-id="724fb-109">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="724fb-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="724fb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="724fb-110">EXAMPLES</span></span>

### <span data-ttu-id="724fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="724fb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="724fb-112">Otaguj kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="724fb-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="724fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724fb-113">PARAMETERS</span></span>

### <span data-ttu-id="724fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724fb-114">-DefaultProfile</span></span>
<span data-ttu-id="724fb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="724fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="724fb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="724fb-116">-InputObject</span></span>
<span data-ttu-id="724fb-117">Obiekt PSController, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="724fb-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="724fb-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="724fb-118">-Name</span></span>
<span data-ttu-id="724fb-119">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="724fb-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="724fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="724fb-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="724fb-121">Resource group name</span></span>

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

### <span data-ttu-id="724fb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="724fb-122">-ResourceId</span></span>
<span data-ttu-id="724fb-123">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="724fb-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="724fb-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="724fb-124">-Tag</span></span>
<span data-ttu-id="724fb-125">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="724fb-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="724fb-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="724fb-126">-Confirm</span></span>
<span data-ttu-id="724fb-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="724fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="724fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724fb-128">-WhatIf</span></span>
<span data-ttu-id="724fb-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="724fb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724fb-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="724fb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="724fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724fb-131">CommonParameters</span></span>
<span data-ttu-id="724fb-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724fb-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724fb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724fb-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="724fb-134">INPUTS</span></span>

### <span data-ttu-id="724fb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="724fb-135">System.String</span></span>

### <span data-ttu-id="724fb-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="724fb-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="724fb-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="724fb-137">OUTPUTS</span></span>

### <span data-ttu-id="724fb-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="724fb-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="724fb-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="724fb-139">NOTES</span></span>

## <span data-ttu-id="724fb-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="724fb-140">RELATED LINKS</span></span>
