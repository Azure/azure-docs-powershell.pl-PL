---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052969"
---
# <span data-ttu-id="ecc5a-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="ecc5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc5a-103">Usuwa publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="ecc5a-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="ecc5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecc5a-104">SYNTAX</span></span>

### <span data-ttu-id="ecc5a-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ecc5a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc5a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc5a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc5a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc5a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ecc5a-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc5a-109">Polecenie cmdlet **Remove-AzPublicIpPrefix** usuwa publiczny prefiks IP usługi Azure, o ile nie przydzielono mu publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="ecc5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecc5a-110">EXAMPLES</span></span>

### <span data-ttu-id="ecc5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ecc5a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="ecc5a-112">Usuwa publiczny prefiks IP z nazwą $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="ecc5a-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="ecc5a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecc5a-113">PARAMETERS</span></span>

### <span data-ttu-id="ecc5a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecc5a-114">-AsJob</span></span>
<span data-ttu-id="ecc5a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ecc5a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecc5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc5a-116">-DefaultProfile</span></span>
<span data-ttu-id="ecc5a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc5a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ecc5a-118">-Force</span></span>
<span data-ttu-id="ecc5a-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ecc5a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ecc5a-120">-InputObject</span></span>
<span data-ttu-id="ecc5a-121">Obiekt PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="ecc5a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ecc5a-122">-Name</span></span>
<span data-ttu-id="ecc5a-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-123">The resource name.</span></span>

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

### <span data-ttu-id="ecc5a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecc5a-124">-PassThru</span></span>
<span data-ttu-id="ecc5a-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecc5a-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ecc5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ecc5a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-128">The resource group name.</span></span>

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

### <span data-ttu-id="ecc5a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc5a-129">-ResourceId</span></span>
<span data-ttu-id="ecc5a-130">Identyfikator zasobu zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="ecc5a-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="ecc5a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecc5a-131">-Confirm</span></span>
<span data-ttu-id="ecc5a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc5a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc5a-133">-WhatIf</span></span>
<span data-ttu-id="ecc5a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc5a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc5a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc5a-136">CommonParameters</span></span>
<span data-ttu-id="ecc5a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc5a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc5a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc5a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecc5a-139">INPUTS</span></span>

### <span data-ttu-id="ecc5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc5a-140">System.String</span></span>

### <span data-ttu-id="ecc5a-141">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="ecc5a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecc5a-142">OUTPUTS</span></span>

### <span data-ttu-id="ecc5a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecc5a-143">System.Boolean</span></span>

## <span data-ttu-id="ecc5a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecc5a-144">NOTES</span></span>

## <span data-ttu-id="ecc5a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecc5a-145">RELATED LINKS</span></span>

[<span data-ttu-id="ecc5a-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="ecc5a-147">Nowe — AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="ecc5a-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ecc5a-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
