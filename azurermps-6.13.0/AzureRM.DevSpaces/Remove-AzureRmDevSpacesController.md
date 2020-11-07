---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718605"
---
# <span data-ttu-id="b2644-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="b2644-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="b2644-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2644-102">SYNOPSIS</span></span>
<span data-ttu-id="b2644-103">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="b2644-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2644-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2644-104">SYNTAX</span></span>

### <span data-ttu-id="b2644-105">DevSpacesControllerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2644-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2644-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2644-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2644-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2644-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2644-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2644-108">DESCRIPTION</span></span>
<span data-ttu-id="b2644-109">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="b2644-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="b2644-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2644-110">EXAMPLES</span></span>

### <span data-ttu-id="b2644-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2644-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="b2644-112">Usuń kontroler DevSpaces o nazwie devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="b2644-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="b2644-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2644-113">PARAMETERS</span></span>

### <span data-ttu-id="b2644-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2644-114">-AsJob</span></span>
<span data-ttu-id="b2644-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2644-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2644-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2644-116">-DefaultProfile</span></span>
<span data-ttu-id="b2644-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2644-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2644-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2644-118">-InputObject</span></span>
<span data-ttu-id="b2644-119">Obiekt PSController, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b2644-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b2644-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2644-120">-Name</span></span>
<span data-ttu-id="b2644-121">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="b2644-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="b2644-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2644-122">-PassThru</span></span>
<span data-ttu-id="b2644-123">Zwraca wartość PRAWDA, jeśli usuwanie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b2644-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="b2644-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2644-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2644-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b2644-125">Resource group name</span></span>

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

### <span data-ttu-id="b2644-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2644-126">-ResourceId</span></span>
<span data-ttu-id="b2644-127">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="b2644-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="b2644-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2644-128">-Confirm</span></span>
<span data-ttu-id="b2644-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2644-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2644-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2644-130">-WhatIf</span></span>
<span data-ttu-id="b2644-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2644-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2644-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2644-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2644-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2644-133">CommonParameters</span></span>
<span data-ttu-id="b2644-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2644-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2644-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2644-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2644-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2644-136">INPUTS</span></span>

### <span data-ttu-id="b2644-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b2644-137">System.String</span></span>

### <span data-ttu-id="b2644-138">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="b2644-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="b2644-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2644-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b2644-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2644-140">OUTPUTS</span></span>

### <span data-ttu-id="b2644-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2644-141">System.Boolean</span></span>

## <span data-ttu-id="b2644-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2644-142">NOTES</span></span>

## <span data-ttu-id="b2644-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2644-143">RELATED LINKS</span></span>
