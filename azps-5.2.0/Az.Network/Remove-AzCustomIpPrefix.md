---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327437"
---
# <span data-ttu-id="bf7bc-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="bf7bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7bc-103">Usuwa CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="bf7bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf7bc-104">SYNTAX</span></span>

### <span data-ttu-id="bf7bc-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf7bc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7bc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf7bc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7bc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf7bc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf7bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bf7bc-108">DESCRIPTION</span></span>
<span data-ttu-id="bf7bc-109">Polecenie cmdlet **Remove-AzCustomIpPrefix** usuwa CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="bf7bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf7bc-110">EXAMPLES</span></span>

### <span data-ttu-id="bf7bc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf7bc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="bf7bc-112">Usuwa CustomIpPrefix o nazwie $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="bf7bc-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="bf7bc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf7bc-113">PARAMETERS</span></span>

### <span data-ttu-id="bf7bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf7bc-114">-AsJob</span></span>
<span data-ttu-id="bf7bc-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bf7bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf7bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7bc-116">-DefaultProfile</span></span>
<span data-ttu-id="bf7bc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf7bc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bf7bc-118">-Force</span></span>
<span data-ttu-id="bf7bc-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bf7bc-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf7bc-120">-InputObject</span></span>
<span data-ttu-id="bf7bc-121">Obiekt customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7bc-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf7bc-122">-Name</span></span>
<span data-ttu-id="bf7bc-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf7bc-124">-PassThru</span></span>
<span data-ttu-id="bf7bc-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf7bc-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf7bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf7bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf7bc-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7bc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf7bc-129">-ResourceId</span></span>
<span data-ttu-id="bf7bc-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7bc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf7bc-131">-Confirm</span></span>
<span data-ttu-id="bf7bc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf7bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf7bc-133">-WhatIf</span></span>
<span data-ttu-id="bf7bc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf7bc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf7bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7bc-136">CommonParameters</span></span>
<span data-ttu-id="bf7bc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf7bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7bc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf7bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7bc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf7bc-139">INPUTS</span></span>

### <span data-ttu-id="bf7bc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf7bc-140">System.String</span></span>

### <span data-ttu-id="bf7bc-141">Microsoft. Azure. Commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="bf7bc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf7bc-142">OUTPUTS</span></span>

### <span data-ttu-id="bf7bc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf7bc-143">System.Boolean</span></span>

## <span data-ttu-id="bf7bc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf7bc-144">NOTES</span></span>

## <span data-ttu-id="bf7bc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf7bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf7bc-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="bf7bc-147">Nowe — AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="bf7bc-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bf7bc-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)