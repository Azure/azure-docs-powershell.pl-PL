---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 2a94d74fb8c6ba6cc9f6c2873269f3009c2f7e9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709926"
---
# <span data-ttu-id="44889-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="44889-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="44889-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44889-102">SYNOPSIS</span></span>
<span data-ttu-id="44889-103">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="44889-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="44889-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44889-104">SYNTAX</span></span>

### <span data-ttu-id="44889-105">DevSpacesControllerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44889-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44889-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44889-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44889-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44889-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44889-108">Opis</span><span class="sxs-lookup"><span data-stu-id="44889-108">DESCRIPTION</span></span>
<span data-ttu-id="44889-109">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="44889-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="44889-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44889-110">EXAMPLES</span></span>

### <span data-ttu-id="44889-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44889-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="44889-112">Znakowanie DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="44889-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="44889-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44889-113">PARAMETERS</span></span>

### <span data-ttu-id="44889-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44889-114">-DefaultProfile</span></span>
<span data-ttu-id="44889-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44889-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44889-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44889-116">-InputObject</span></span>
<span data-ttu-id="44889-117">Obiekt PSController, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="44889-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="44889-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44889-118">-Name</span></span>
<span data-ttu-id="44889-119">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="44889-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="44889-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44889-120">-ResourceGroupName</span></span>
<span data-ttu-id="44889-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44889-121">Resource group name</span></span>

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

### <span data-ttu-id="44889-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44889-122">-ResourceId</span></span>
<span data-ttu-id="44889-123">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="44889-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="44889-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="44889-124">-Tag</span></span>
<span data-ttu-id="44889-125">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="44889-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="44889-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44889-126">-Confirm</span></span>
<span data-ttu-id="44889-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44889-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44889-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44889-128">-WhatIf</span></span>
<span data-ttu-id="44889-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44889-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44889-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44889-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44889-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44889-131">CommonParameters</span></span>
<span data-ttu-id="44889-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44889-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44889-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44889-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44889-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44889-134">INPUTS</span></span>

### <span data-ttu-id="44889-135">System. String</span><span class="sxs-lookup"><span data-stu-id="44889-135">System.String</span></span>

### <span data-ttu-id="44889-136">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="44889-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="44889-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44889-137">OUTPUTS</span></span>

### <span data-ttu-id="44889-138">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="44889-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="44889-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44889-139">NOTES</span></span>

## <span data-ttu-id="44889-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44889-140">RELATED LINKS</span></span>
