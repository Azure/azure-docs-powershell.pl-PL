---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328893"
---
# <span data-ttu-id="66c85-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="66c85-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="66c85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66c85-102">SYNOPSIS</span></span>
<span data-ttu-id="66c85-103">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="66c85-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="66c85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66c85-104">SYNTAX</span></span>

### <span data-ttu-id="66c85-105">DevSpacesControllerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="66c85-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c85-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c85-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c85-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c85-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c85-108">Opis</span><span class="sxs-lookup"><span data-stu-id="66c85-108">DESCRIPTION</span></span>
<span data-ttu-id="66c85-109">Usuń kontroler DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="66c85-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="66c85-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66c85-110">EXAMPLES</span></span>

### <span data-ttu-id="66c85-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66c85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="66c85-112">Usuń kontroler DevSpaces o nazwie devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="66c85-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="66c85-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66c85-113">PARAMETERS</span></span>

### <span data-ttu-id="66c85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66c85-114">-AsJob</span></span>
<span data-ttu-id="66c85-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66c85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66c85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c85-116">-DefaultProfile</span></span>
<span data-ttu-id="66c85-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66c85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c85-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66c85-118">-InputObject</span></span>
<span data-ttu-id="66c85-119">Obiekt PSController, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="66c85-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="66c85-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66c85-120">-Name</span></span>
<span data-ttu-id="66c85-121">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="66c85-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="66c85-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c85-122">-PassThru</span></span>
<span data-ttu-id="66c85-123">Zwraca wartość PRAWDA, jeśli usuwanie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="66c85-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="66c85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c85-124">-ResourceGroupName</span></span>
<span data-ttu-id="66c85-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="66c85-125">Resource group name</span></span>

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

### <span data-ttu-id="66c85-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c85-126">-ResourceId</span></span>
<span data-ttu-id="66c85-127">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="66c85-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="66c85-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66c85-128">-Confirm</span></span>
<span data-ttu-id="66c85-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66c85-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c85-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c85-130">-WhatIf</span></span>
<span data-ttu-id="66c85-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66c85-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c85-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66c85-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c85-133">CommonParameters</span></span>
<span data-ttu-id="66c85-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c85-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c85-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c85-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66c85-136">INPUTS</span></span>

### <span data-ttu-id="66c85-137">System. String</span><span class="sxs-lookup"><span data-stu-id="66c85-137">System.String</span></span>

### <span data-ttu-id="66c85-138">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="66c85-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="66c85-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66c85-139">OUTPUTS</span></span>

### <span data-ttu-id="66c85-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66c85-140">System.Boolean</span></span>

## <span data-ttu-id="66c85-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66c85-141">NOTES</span></span>

## <span data-ttu-id="66c85-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66c85-142">RELATED LINKS</span></span>
