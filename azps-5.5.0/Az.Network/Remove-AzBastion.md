---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202585"
---
# <span data-ttu-id="c2f5e-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c2f5e-101">Remove-AzBastion</span></span>

## <span data-ttu-id="c2f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f5e-103">Usuwa zasób zasobów zasobów pracy.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="c2f5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2f5e-104">SYNTAX</span></span>

### <span data-ttu-id="c2f5e-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="c2f5e-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2f5e-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f5e-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f5e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f5e-109">Usuwa zasób rów. Przykład1 powoduje usunięcie grupy przy użyciu jej nazwa_grupy zasobów i nazwa_zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="c2f5e-110">W przykładzie2 rytacja jest usuwana przy użyciu obiektu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="c2f5e-111">W przykładzie 3 rycowanie jest usuwane przy użyciu jego obiektu.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="c2f5e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2f5e-112">EXAMPLES</span></span>

### <span data-ttu-id="c2f5e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2f5e-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="c2f5e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2f5e-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="c2f5e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c2f5e-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="c2f5e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2f5e-116">PARAMETERS</span></span>

### <span data-ttu-id="c2f5e-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2f5e-117">-Confirm</span></span>
<span data-ttu-id="c2f5e-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f5e-119">-DefaultProfile</span></span>
<span data-ttu-id="c2f5e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c2f5e-121">-Force</span></span>
<span data-ttu-id="c2f5e-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-122">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f5e-123">-InputObject</span></span>
<span data-ttu-id="c2f5e-124">Obiekt Bastion do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2f5e-125">-Name</span></span>
<span data-ttu-id="c2f5e-126">Nazwa zasobu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2f5e-127">-PassThru</span></span>
<span data-ttu-id="c2f5e-128">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f5e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2f5e-130">Nazwa grupy zasobów, w której istnieje grupowanie.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f5e-131">-ResourceId</span></span>
<span data-ttu-id="c2f5e-132">Identyfikator zasobu Azure, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f5e-133">-WhatIf</span></span>
<span data-ttu-id="c2f5e-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f5e-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f5e-136">CommonParameters</span></span>
<span data-ttu-id="c2f5e-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f5e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2f5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f5e-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2f5e-139">INPUTS</span></span>

### <span data-ttu-id="c2f5e-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="c2f5e-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="c2f5e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c2f5e-141">System.String</span></span>

## <span data-ttu-id="c2f5e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2f5e-142">OUTPUTS</span></span>

### <span data-ttu-id="c2f5e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c2f5e-143">System.Boolean</span></span>

## <span data-ttu-id="c2f5e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2f5e-144">NOTES</span></span>

## <span data-ttu-id="c2f5e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2f5e-145">RELATED LINKS</span></span>
[<span data-ttu-id="c2f5e-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c2f5e-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="c2f5e-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c2f5e-147">New-AzBastion</span></span>](./New-AzBastion.md)