---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053048"
---
# <span data-ttu-id="36011-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="36011-101">Remove-AzBastion</span></span>

## <span data-ttu-id="36011-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36011-102">SYNOPSIS</span></span>
<span data-ttu-id="36011-103">Usuwa zasób Bastion.</span><span class="sxs-lookup"><span data-stu-id="36011-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="36011-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36011-104">SYNTAX</span></span>

### <span data-ttu-id="36011-105">ByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36011-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36011-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36011-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36011-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36011-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36011-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36011-108">DESCRIPTION</span></span>
<span data-ttu-id="36011-109">Usuwa zasób Bastion. Example1 usuwa Bastion przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="36011-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="36011-110">Example2 usuwa Bastion przy użyciu obiektu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="36011-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="36011-111">Example3 usuwa Bastion za pomocą obiektu.</span><span class="sxs-lookup"><span data-stu-id="36011-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="36011-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36011-112">EXAMPLES</span></span>

### <span data-ttu-id="36011-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36011-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="36011-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36011-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="36011-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="36011-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="36011-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36011-116">PARAMETERS</span></span>

### <span data-ttu-id="36011-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36011-117">-Confirm</span></span>
<span data-ttu-id="36011-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36011-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36011-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36011-119">-DefaultProfile</span></span>
<span data-ttu-id="36011-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36011-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36011-121">-Force</span><span class="sxs-lookup"><span data-stu-id="36011-121">-Force</span></span>
<span data-ttu-id="36011-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36011-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36011-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36011-123">-InputObject</span></span>
<span data-ttu-id="36011-124">Obiekt Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="36011-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="36011-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36011-125">-Name</span></span>
<span data-ttu-id="36011-126">Nazwa zasobu Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="36011-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="36011-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36011-127">-PassThru</span></span>
<span data-ttu-id="36011-128">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="36011-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="36011-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36011-129">-ResourceGroupName</span></span>
<span data-ttu-id="36011-130">Nazwa grupy zasobów, na której Bastion istnieje.</span><span class="sxs-lookup"><span data-stu-id="36011-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="36011-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36011-131">-ResourceId</span></span>
<span data-ttu-id="36011-132">Identyfikator zasobu platformy Azure dla Bastion, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="36011-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="36011-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36011-133">-WhatIf</span></span>
<span data-ttu-id="36011-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36011-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36011-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36011-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36011-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36011-136">CommonParameters</span></span>
<span data-ttu-id="36011-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36011-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36011-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36011-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36011-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36011-139">INPUTS</span></span>

### <span data-ttu-id="36011-140">Microsoft. Azure. Commands. Network. models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="36011-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="36011-141">System. String</span><span class="sxs-lookup"><span data-stu-id="36011-141">System.String</span></span>

## <span data-ttu-id="36011-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36011-142">OUTPUTS</span></span>

### <span data-ttu-id="36011-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36011-143">System.Boolean</span></span>

## <span data-ttu-id="36011-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36011-144">NOTES</span></span>

## <span data-ttu-id="36011-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36011-145">RELATED LINKS</span></span>
[<span data-ttu-id="36011-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="36011-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="36011-147">Nowe — AzBastion</span><span class="sxs-lookup"><span data-stu-id="36011-147">New-AzBastion</span></span>](./New-AzBastion.md)