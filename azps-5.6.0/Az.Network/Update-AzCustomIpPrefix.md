---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 9d0bca8be88c0448916df27544ce35bf7a6ddee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951706"
---
# <span data-ttu-id="3832a-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="3832a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3832a-102">SYNOPSIS</span></span>
<span data-ttu-id="3832a-103">Aktualizacja poprawki CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="3832a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3832a-104">SYNTAX</span></span>

### <span data-ttu-id="3832a-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3832a-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3832a-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3832a-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3832a-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3832a-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3832a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3832a-108">DESCRIPTION</span></span>
<span data-ttu-id="3832a-109">Polecenie **cmdlet Update-AzCustomIpPrefix** umożliwia użytkownikowi prowizję lub zlikwidowanie jego poprawki CustomIpPrefix albo edytowanie tagów zasobu.</span><span class="sxs-lookup"><span data-stu-id="3832a-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="3832a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3832a-110">EXAMPLES</span></span>

### <span data-ttu-id="3832a-111">Przykład 1. Prowizja dla poprawki CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="3832a-112">Powyższe polecenie rozpocznie proces uruchamiania poprawki CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3832a-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="3832a-113">Przykład 2. Zlikwidowanie poprawki CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="3832a-114">Powyższe polecenie rozpocznie proces uruchamiania poprawki CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3832a-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="3832a-115">Przykład 3. Aktualizowanie tagów dla poprawki CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="3832a-116">Powyższe polecenie zaktualizuje tagi dla poprawki CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3832a-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="3832a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3832a-117">PARAMETERS</span></span>

### <span data-ttu-id="3832a-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3832a-118">-AsJob</span></span>
<span data-ttu-id="3832a-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3832a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3832a-120">— Prowizja</span><span class="sxs-lookup"><span data-stu-id="3832a-120">-Commission</span></span>
<span data-ttu-id="3832a-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3832a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3832a-122">- Dekodowanie</span><span class="sxs-lookup"><span data-stu-id="3832a-122">-Decomission</span></span>
<span data-ttu-id="3832a-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3832a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3832a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3832a-124">-DefaultProfile</span></span>
<span data-ttu-id="3832a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3832a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3832a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3832a-126">-InputObject</span></span>
<span data-ttu-id="3832a-127">Ustawienie niestandardowego rozwiązaniaIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3832a-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3832a-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3832a-128">-Name</span></span>
<span data-ttu-id="3832a-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3832a-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3832a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3832a-130">-ResourceGroupName</span></span>
<span data-ttu-id="3832a-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3832a-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3832a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3832a-132">-ResourceId</span></span>
<span data-ttu-id="3832a-133">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3832a-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3832a-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="3832a-134">-Tag</span></span>
<span data-ttu-id="3832a-135">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3832a-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3832a-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3832a-136">-Confirm</span></span>
<span data-ttu-id="3832a-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3832a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3832a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3832a-138">-WhatIf</span></span>
<span data-ttu-id="3832a-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3832a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3832a-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3832a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3832a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3832a-141">CommonParameters</span></span>
<span data-ttu-id="3832a-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3832a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3832a-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3832a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3832a-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3832a-144">INPUTS</span></span>

### <span data-ttu-id="3832a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3832a-145">System.String</span></span>

### <span data-ttu-id="3832a-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="3832a-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3832a-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3832a-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3832a-148">OUTPUTS</span></span>

### <span data-ttu-id="3832a-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="3832a-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3832a-150">NOTES</span></span>

## <span data-ttu-id="3832a-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3832a-151">RELATED LINKS</span></span>

[<span data-ttu-id="3832a-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="3832a-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="3832a-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3832a-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)