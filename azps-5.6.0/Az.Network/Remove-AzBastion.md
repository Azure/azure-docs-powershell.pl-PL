---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: b58ffa98f3f35a8e8f87785e4d7abb703aa9b90e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976666"
---
# <span data-ttu-id="b24c5-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="b24c5-101">Remove-AzBastion</span></span>

## <span data-ttu-id="b24c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b24c5-103">Usuwa zasób rów.</span><span class="sxs-lookup"><span data-stu-id="b24c5-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="b24c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b24c5-104">SYNTAX</span></span>

### <span data-ttu-id="b24c5-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="b24c5-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b24c5-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24c5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b24c5-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b24c5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b24c5-108">DESCRIPTION</span></span>
<span data-ttu-id="b24c5-109">Usuwa zasób rów. Przykład1 powoduje usunięcie grupy przy użyciu jej nazwa_grupy zasobów i nazwa_zasobu.</span><span class="sxs-lookup"><span data-stu-id="b24c5-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="b24c5-110">Przykład 2. Usunięcie tego rąbka przy użyciu jego obiektu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="b24c5-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="b24c5-111">W przykładzie 3 jest usuwana równanie przy użyciu jego obiektu.</span><span class="sxs-lookup"><span data-stu-id="b24c5-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="b24c5-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b24c5-112">EXAMPLES</span></span>

### <span data-ttu-id="b24c5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b24c5-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="b24c5-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b24c5-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="b24c5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b24c5-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="b24c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24c5-116">PARAMETERS</span></span>

### <span data-ttu-id="b24c5-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b24c5-117">-Confirm</span></span>
<span data-ttu-id="b24c5-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b24c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b24c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24c5-119">-DefaultProfile</span></span>
<span data-ttu-id="b24c5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b24c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24c5-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b24c5-121">-Force</span></span>
<span data-ttu-id="b24c5-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b24c5-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b24c5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b24c5-123">-InputObject</span></span>
<span data-ttu-id="b24c5-124">Obiekt Bastion do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b24c5-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="b24c5-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b24c5-125">-Name</span></span>
<span data-ttu-id="b24c5-126">Nazwa zasobu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b24c5-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="b24c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b24c5-127">-PassThru</span></span>
<span data-ttu-id="b24c5-128">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="b24c5-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="b24c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b24c5-130">Nazwa grupy zasobów, dla której istnieje grupowanie.</span><span class="sxs-lookup"><span data-stu-id="b24c5-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="b24c5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24c5-131">-ResourceId</span></span>
<span data-ttu-id="b24c5-132">Identyfikator zasobu Azure, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b24c5-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="b24c5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b24c5-133">-WhatIf</span></span>
<span data-ttu-id="b24c5-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b24c5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b24c5-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b24c5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b24c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24c5-136">CommonParameters</span></span>
<span data-ttu-id="b24c5-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24c5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b24c5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24c5-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b24c5-139">INPUTS</span></span>

### <span data-ttu-id="b24c5-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="b24c5-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="b24c5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b24c5-141">System.String</span></span>

## <span data-ttu-id="b24c5-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b24c5-142">OUTPUTS</span></span>

### <span data-ttu-id="b24c5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b24c5-143">System.Boolean</span></span>

## <span data-ttu-id="b24c5-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b24c5-144">NOTES</span></span>

## <span data-ttu-id="b24c5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b24c5-145">RELATED LINKS</span></span>
[<span data-ttu-id="b24c5-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="b24c5-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="b24c5-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="b24c5-147">New-AzBastion</span></span>](./New-AzBastion.md)