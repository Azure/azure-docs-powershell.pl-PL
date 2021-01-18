---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499221"
---
# <span data-ttu-id="07674-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="07674-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="07674-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07674-102">SYNOPSIS</span></span>
<span data-ttu-id="07674-103">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="07674-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="07674-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07674-104">SYNTAX</span></span>

### <span data-ttu-id="07674-105">DevSpacesControllerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="07674-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07674-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07674-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07674-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07674-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07674-108">Opis</span><span class="sxs-lookup"><span data-stu-id="07674-108">DESCRIPTION</span></span>
<span data-ttu-id="07674-109">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="07674-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="07674-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07674-110">EXAMPLES</span></span>

### <span data-ttu-id="07674-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07674-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="07674-112">Oznacz kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="07674-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="07674-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07674-113">PARAMETERS</span></span>

### <span data-ttu-id="07674-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07674-114">-DefaultProfile</span></span>
<span data-ttu-id="07674-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07674-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07674-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="07674-116">-InputObject</span></span>
<span data-ttu-id="07674-117">Obiekt PSController, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="07674-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="07674-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07674-118">-Name</span></span>
<span data-ttu-id="07674-119">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="07674-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="07674-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07674-120">-ResourceGroupName</span></span>
<span data-ttu-id="07674-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="07674-121">Resource group name</span></span>

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

### <span data-ttu-id="07674-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07674-122">-ResourceId</span></span>
<span data-ttu-id="07674-123">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="07674-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="07674-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="07674-124">-Tag</span></span>
<span data-ttu-id="07674-125">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="07674-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="07674-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07674-126">-Confirm</span></span>
<span data-ttu-id="07674-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07674-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07674-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07674-128">-WhatIf</span></span>
<span data-ttu-id="07674-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07674-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07674-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07674-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07674-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07674-131">CommonParameters</span></span>
<span data-ttu-id="07674-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07674-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07674-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07674-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07674-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07674-134">INPUTS</span></span>

### <span data-ttu-id="07674-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07674-135">System.String</span></span>

### <span data-ttu-id="07674-136">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="07674-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="07674-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07674-137">OUTPUTS</span></span>

### <span data-ttu-id="07674-138">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="07674-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="07674-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07674-139">NOTES</span></span>

## <span data-ttu-id="07674-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07674-140">RELATED LINKS</span></span>
