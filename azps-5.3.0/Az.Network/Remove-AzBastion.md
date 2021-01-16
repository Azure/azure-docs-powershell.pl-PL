---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385287"
---
# <span data-ttu-id="46d89-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="46d89-101">Remove-AzBastion</span></span>

## <span data-ttu-id="46d89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46d89-102">SYNOPSIS</span></span>
<span data-ttu-id="46d89-103">Usuwa zasób Bastion.</span><span class="sxs-lookup"><span data-stu-id="46d89-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="46d89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46d89-104">SYNTAX</span></span>

### <span data-ttu-id="46d89-105">ByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46d89-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d89-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46d89-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d89-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46d89-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d89-108">Opis</span><span class="sxs-lookup"><span data-stu-id="46d89-108">DESCRIPTION</span></span>
<span data-ttu-id="46d89-109">Usuwa zasób Bastion. Example1 usuwa Bastion przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="46d89-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="46d89-110">Example2 usuwa Bastion przy użyciu obiektu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="46d89-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="46d89-111">Example3 usuwa Bastion za pomocą obiektu.</span><span class="sxs-lookup"><span data-stu-id="46d89-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="46d89-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46d89-112">EXAMPLES</span></span>

### <span data-ttu-id="46d89-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46d89-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="46d89-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46d89-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="46d89-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="46d89-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="46d89-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46d89-116">PARAMETERS</span></span>

### <span data-ttu-id="46d89-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46d89-117">-Confirm</span></span>
<span data-ttu-id="46d89-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d89-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d89-119">-DefaultProfile</span></span>
<span data-ttu-id="46d89-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46d89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d89-121">-Force</span><span class="sxs-lookup"><span data-stu-id="46d89-121">-Force</span></span>
<span data-ttu-id="46d89-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46d89-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46d89-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46d89-123">-InputObject</span></span>
<span data-ttu-id="46d89-124">Obiekt Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="46d89-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="46d89-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46d89-125">-Name</span></span>
<span data-ttu-id="46d89-126">Nazwa zasobu Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="46d89-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="46d89-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d89-127">-PassThru</span></span>
<span data-ttu-id="46d89-128">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="46d89-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="46d89-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d89-129">-ResourceGroupName</span></span>
<span data-ttu-id="46d89-130">Nazwa grupy zasobów, na której Bastion istnieje.</span><span class="sxs-lookup"><span data-stu-id="46d89-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="46d89-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46d89-131">-ResourceId</span></span>
<span data-ttu-id="46d89-132">Identyfikator zasobu platformy Azure dla Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="46d89-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="46d89-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d89-133">-WhatIf</span></span>
<span data-ttu-id="46d89-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d89-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d89-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46d89-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d89-136">CommonParameters</span></span>
<span data-ttu-id="46d89-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d89-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d89-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d89-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46d89-139">INPUTS</span></span>

### <span data-ttu-id="46d89-140">Microsoft. Azure. Commands. Network. models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="46d89-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="46d89-141">System. String</span><span class="sxs-lookup"><span data-stu-id="46d89-141">System.String</span></span>

## <span data-ttu-id="46d89-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46d89-142">OUTPUTS</span></span>

### <span data-ttu-id="46d89-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46d89-143">System.Boolean</span></span>

## <span data-ttu-id="46d89-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46d89-144">NOTES</span></span>

## <span data-ttu-id="46d89-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46d89-145">RELATED LINKS</span></span>
[<span data-ttu-id="46d89-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="46d89-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="46d89-147">Nowe — AzBastion</span><span class="sxs-lookup"><span data-stu-id="46d89-147">New-AzBastion</span></span>](./New-AzBastion.md)