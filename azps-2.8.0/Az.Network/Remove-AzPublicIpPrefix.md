---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869687"
---
# <span data-ttu-id="b25f8-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="b25f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b25f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b25f8-103">Usuwa publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="b25f8-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="b25f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b25f8-104">SYNTAX</span></span>

### <span data-ttu-id="b25f8-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b25f8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b25f8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b25f8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b25f8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b25f8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b25f8-108">DESCRIPTION</span></span>
<span data-ttu-id="b25f8-109">Polecenie cmdlet **Remove-AzPublicIpPrefix** usuwa publiczny prefiks IP usługi Azure, o ile nie przydzielono mu publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b25f8-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="b25f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b25f8-110">EXAMPLES</span></span>

### <span data-ttu-id="b25f8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b25f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="b25f8-112">Usuwa publiczny prefiks IP z nazwą $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="b25f8-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="b25f8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b25f8-113">PARAMETERS</span></span>

### <span data-ttu-id="b25f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b25f8-114">-AsJob</span></span>
<span data-ttu-id="b25f8-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b25f8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b25f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25f8-116">-DefaultProfile</span></span>
<span data-ttu-id="b25f8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b25f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25f8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b25f8-118">-Force</span></span>
<span data-ttu-id="b25f8-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b25f8-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b25f8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b25f8-120">-InputObject</span></span>
<span data-ttu-id="b25f8-121">Obiekt PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b25f8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b25f8-122">-Name</span></span>
<span data-ttu-id="b25f8-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b25f8-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25f8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b25f8-124">-PassThru</span></span>
<span data-ttu-id="b25f8-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b25f8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b25f8-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b25f8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b25f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="b25f8-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b25f8-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25f8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b25f8-129">-ResourceId</span></span>
<span data-ttu-id="b25f8-130">Identyfikator zasobu zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="b25f8-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25f8-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b25f8-131">-Confirm</span></span>
<span data-ttu-id="b25f8-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b25f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b25f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25f8-133">-WhatIf</span></span>
<span data-ttu-id="b25f8-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b25f8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25f8-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b25f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b25f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25f8-136">CommonParameters</span></span>
<span data-ttu-id="b25f8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25f8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25f8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b25f8-139">INPUTS</span></span>

### <span data-ttu-id="b25f8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b25f8-140">System.String</span></span>

### <span data-ttu-id="b25f8-141">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="b25f8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b25f8-142">OUTPUTS</span></span>

### <span data-ttu-id="b25f8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b25f8-143">System.Boolean</span></span>

## <span data-ttu-id="b25f8-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b25f8-144">NOTES</span></span>

## <span data-ttu-id="b25f8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b25f8-145">RELATED LINKS</span></span>

[<span data-ttu-id="b25f8-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="b25f8-147">Nowe — AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="b25f8-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b25f8-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
